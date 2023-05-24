---
title: 實驗報告中使用的統計計算
description: 進一步瞭解執行實驗報告時使用的統計計算
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: b3336381-bc73-4c8f-938f-f10fe37305b0
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '961'
ht-degree: 4%

---

# 实验报表中的统计计算 {#experiment-report-calculations}

>[!BEGINSHADEBOX]

本文档包括以下内容：

* [内容体验入门](get-started-experiment.md)
* [创建内容试验](content-experiment.md)
* [了解统计计算](experiment-calculations.md)
* [配置实验报表](reporting-configuration.md)
* **[实验报表中的统计计算](experiment-report-calculations.md)**

>[!ENDSHADEBOX]

本頁會記錄Adobe Journey Optimizer行銷活動的Experimentation報告中使用的詳細統計計算。

請注意，本頁僅供技術使用者使用。

## 转化率

轉換率或 **平均值**， μ<sub>ν</sub> 針對每個處理 `ν` 在實驗中，定義為量度加總與指派給該量度的設定檔數之間的比率，N<sub>ν</sub>：

![](assets/statistical_1.png){width="125" align="center"}

這裡，Y<sub>iν</sub> 是每個設定檔的目標量度值 `i`，已指派給指定變體 *ν*. 當目標量度是「唯一」量度時（即是執行特定動作的設定檔數計數），會顯示為轉換率，並會以百分比格式化。 當量度是「計數」或「總值」量度（分別例如電子郵件開啟次數、收入）時，該量度的平均估計值會顯示為「每個設定檔計數」或「每個設定檔的值」。

如有需要，範例標準差會與運算式搭配使用：

![](assets/statistical_2.png){width="225" align="center"}

## 提升 {#lift}

變體之間的提升度  *ν*、和控制變體  *ν<sub>0</sub>* 是轉換率中的相對「差異」，其定義如下，其中個別轉換率如上所定義。 這會以百分比顯示。

![](assets/statistical_3.png){width="125" align="center"}

</br>

## 適用於個別處理的隨時有效信賴區間

Journey Experimentation面板會顯示實驗中個別處理作業的「隨時有效」信賴區間（信賴序列）。

個別變體的信賴序列 `ν` 是Adobe所用統計方法的核心。 您可以在下列位置找到其定義： [此頁面](https://doi.org/10.48550/arXiv.2103.06476) (轉載自 [Waudby-Smith等])。

如果您有興趣估計目標引數 `ψ` 例如，實驗中的變體轉換率，「固定時間」信賴區間(CI)序列和時間一致信賴序列(CS)之間的二分法可以概括如下：

![](assets/statistical_4.png){width="500" align="center"}

對於規則信賴區間，目標引數落在值ċ範圍內的機率保證<sub>n</sub> 只對下列的單一固定值有效： `n` (其中 `n` 為樣本數)。 相反地，對於信賴序列，我們保證在任何時候/所有樣本大小值 `t`，則感興趣之引數的「true」值位於界限內。

這隱含幾項對線上測試非常重要的深層含意：

* CS可在有新資料可用時選擇性更新。
* 實驗可以持續監控、自動停止或繼續。
* type-I錯誤會在所有停止時間受到控制，包括資料相關時間。

Adobe使用漸近信賴序列，這適用於具有平均估計值的個別變體 `μ` 具有下列形式：

![](assets/statistical_5.png){width="300" align="center"}

执行:

* `N` 是該變體的單位數。
* `σ` 是標準差預估範例（定義於上文）。
* `α` 是所需的型別I錯誤（或覆蓋範圍錯誤機率）層級。 此值一律設為0.05。
* ρ<sup>2</sup> 是一個常數，可調整CS最緊密的樣本大小。 Adobe已選擇通用值ρ<sup>2</sup> = 10<sup>-2.8</sup>，適用於線上實驗中顯示的轉換率型別。

## 置信度 {#confidence}

Adobe使用的信賴度是「隨時有效」的信賴，這是透過反轉平均處理效果的信賴序列所取得。

更精確地說，在兩個範例中 *t* 測試兩個變體之間的均值差異，變體之間有1:1的對應 *p*-value代表此測試，而信賴區間代表均值。 打個比方，隨時有效 *p*-value可透過反轉平均處理效果估計器的（隨時有效）信賴序列來取得：

![](assets/statistical_6.png){width="200" align="center"}

此處， *E* 是預期。 使用的估算方法是反傾向加權(IPW)估算器。 考慮N = N<sub>0</sub> +N<sub>1</sub> 單位，每個單位的變體指派 `i` 標示為A<sub>i</sub>=0,1如果單位指派給變體 `ν`=0,1. 如果使用者被指派了固定機率（傾向） π<sub>0</sub>，(1-π<sub>0</sub>)，其結果量度為Y<sub>i</sub>，則平均處理效果的IPW估算程式為：

![](assets/statistical_12.png){width="400" align="center"}

注意 *f* 為影響函式，Waudby-Smith等 顯示此估算程式的信賴序列為：

![](assets/statistical_7.png){width="500" align="center"}

以經驗估計值取代指派機率： π<sub>0</sub> = N<sub>0</sub>/N，變數項可以用個別樣本平均估計值μ來表示<sub>0,1</sub> 和標準差估計值，σ<sub>0,1</sub> 作為：

![](assets/statistical_8.png){width="500" align="center"}

接下來，回想一下使用測試統計值z = (μ)進行的一般假設測試<sub>A</sub>-μ<sub>0</sub>/σ<sub>p</sub>)兩者之間有對應關係 `p` — 值和信賴區間：

![](assets/statistical_9.png){width="500" align="center"}

位置 `Φ` 是標準常數的累積分佈。 隨時有效 `p`-values，給定上述定義之平均處理效果的信賴序列，我們可以反轉此關係：

![](assets/statistical_10.png){width="600" align="center"}

最後， **隨時有效的信賴度** 為：

![](assets/statistical_11.png){width="200" align="center"}

## 宣告實驗為具有結論性

對於具有兩個手臂的實驗， Journey Optimizer Experimentation面板會顯示訊息，說明實驗是 **已有結果** 當隨時有效信賴度超過95% （即隨時有效）時 `p`-value低於5%)。

當存在兩個以上的變體時，會套用Bonferonni校正，以控制以族為基礎的錯誤率。 實驗對象： `K` 處理方式以及單一基準（控制）處理方式有 `K-1` 獨立的假設檢驗。 Bonferonni校正表示我們拒絕空值的假設，即如果任何時間都有效，控制項和給定變體具有相等的方法 `p`-value （以上定義）低於臨界值 `α/(K-1)`.

## 績效最佳的手臂

當一個實驗宣告為具有結論性時，會顯示表現最佳的臂。 這是包含控制項的「集合」中，效能最佳（最高平均或轉換率）的臂，以及所有具有 `p` — 值低於Bonferonni臨界值。
