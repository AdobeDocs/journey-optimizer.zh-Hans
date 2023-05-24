---
solution: Journey Optimizer
product: journey optimizer
title: Adobe Journey Optimizer Experimentation使用的統計計算
description: 進一步瞭解執行實驗時使用的統計計算
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
keywords: 內容，實驗，統計，計算
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 3%

---

# 了解统计计算 {#experiment-calculations}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容体验](content-experiment.md)
* **[了解统计计算](experiment-calculations.md)**
* [配置实验报表](reporting-configuration.md)
* [实验报表中的统计计算](experiment-report-calculations.md)

>[!ENDSHADEBOX]

本文說明在Adobe Journey Optimizer中執行實驗時所使用的統計計算。

實驗使用進階統計方法來計算 **信賴序列** 和 **信賴度**，可讓您視需要長時間執行實驗並持續監控結果。

本文說明Experimentation的運作方式，並直覺地介紹Adobe的 **任何時間有效的信賴序列**.

對於專家使用者，技術詳細資訊和參考資料詳見 [此頁面](../campaigns/assets/confidence_sequence_technical_details.pdf).

## 統計測試和控制錯誤 {#statistical-testing}

![](assets/technote_1.png)

如上表所示，許多統計推斷方法的設計目的都是為了控制兩種型別的錯誤：

* **誤判（Type-I錯誤）**：不正確拒絕null假設，但實際上為true。 就線上實驗而言，這表示我們錯誤地斷定結果量度在每個處理之間是不同的，儘管它是相同的。
   </br>在執行實驗之前，我們通常會挑選一個臨界值 `\alpha`. 執行實驗後， `p-value` 已計算，我們拒絕 `null if p < \alpha`. 常用的臨界值為 `\alpha = 0.05`，這表示長遠而言，我們預計每100個實驗中有5個是誤判。

* **誤判負值（型別II錯誤）**：表示我們無法拒絕null假設，儘管它為false。 對於實驗，這表示我們不拒絕Null假設，但實際上它不同。 為了控制這類錯誤，我們的實驗通常需要有足夠的使用者來保證一定的功率，定義為 `1 - \beta`（即1減去II型錯誤的可能性）。

大多數的統計推斷技術會要求您根據您想要決定的效果大小以及錯誤容許度，提前修正樣本大小(`\alpha` 和 `\beta`)之前送達。 不過，Adobe Journey Optimizer的方法旨在讓您持續檢視任何樣本大小的結果。

## Adobe的統計方法：任何時間有效的信賴序列

A **信賴序列** 是連續類比的 **信賴區間**，例如，如果您重複實驗一百次，並計算每個進入實驗新使用者的平均量度估計值及其相關的95%信賴序列。 95%信賴序列會包含您執行100個實驗中的95個中的量度真實值。 每個實驗只能計算一次95%信賴區間，以提供相同的95%覆蓋率保證；而不是針對每個新使用者。 因此，信賴序列可讓您持續監視實驗，而不會增加誤判錯誤率。

單一實驗的信賴序列和信賴區間之間的差異如下圖所示：

![](assets/technote_2.gif)

**信賴序列** 將實驗的焦點轉移到預估而不是假設測試，也就是說，專注於精確估計不同處理之間的方法差異，而不是是否根據統計顯著性臨界值拒絕Null假設。

然而，以類似的方式處理兩者 `p-values`，或 **信賴度**、和 **信賴區間**&#x200B;中，兩者之間也存在某種關係 **信賴序列** 且隨時有效 `p-values`或任何有效的信賴度。 考慮到信賴度等量的熟悉度，Adobe會同時提供 **信賴序列** 以及任何時間對其報表的有效信賴度。

的理論基礎 **信賴序列** 來自隨機變數（稱為烈酒）序列的研究。 以下提供專家閱讀程式時的一些主要結果，但從業者的建議很明確：

>[!NOTE]
>
>信賴序列可以解譯為信賴區間的安全連續類似專案。您可以隨時檢視和解讀實驗中的資料，並安全地停止或繼續實驗。 隨時有效的對應信賴度，或 `p-value`、也是可安全解讀的。

需要注意的是，由於信賴序列是「任何時間有效的」，因此會比在相同樣本大小下使用的固定水平面方法更保守。 信賴序列的界限通常比信賴區間計算更寬，而任何時間的有效信賴將小於固定視界信賴計算。 這種保守主義的好處是，您可以隨時安全地解讀結果。

## 宣告實驗為具有結論性

![](assets/experimentation_report_2.png)

每次檢視實驗報告時，Adobe都會分析到目前為止在實驗中累積的資料，並將在至少一個處理的隨時有效信賴度超過95%臨界值時宣告實驗為「結論性」。

此時，表現最佳的處理（根據轉換率或設定檔標準化量度值）將會在報表畫面頂端反白顯示，並在表格報表中以星號標示。 此決定只會考慮信賴度大於95%的處理以及基準線。

當有兩個以上的處理方法時，Bonferroni校正連結可用來校正多個比較問題，並控制以家庭為基礎的錯誤率。 在此案例中，也可能有多個處理具有大於95%的信賴度，且其信賴區間重疊。 在這種情況下，Adobe Journey Optimizer會宣告轉換率（或設定檔標準化量度值）最高的為績效最佳者。
