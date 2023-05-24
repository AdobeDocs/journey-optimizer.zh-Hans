---
product: experience platform
solution: Experience Platform
title: 自動最佳化模型
description: 進一步瞭解自動最佳化模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: a85de6a9-ece2-43da-8789-e4f8b0e4a0e7
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '1365'
ht-degree: 0%

---

# 自動最佳化模型 {#auto-optimization-model}

自動最佳化模型旨在提供可最大化業務客戶所設定回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能最佳化。

## 限制 {#limitations}

使用自動最佳化模型來進行決策管理時，受限於下列限制：

* 自動最佳化模型不適用於批次決策API。
* 建立模型所需的意見反應必須作為體驗事件傳入中。 此檔案不應自動傳入中 [!DNL Journey Optimizer] 管道。

## 术语 {#terminology}

討論自動最佳化時，下列字詞相當實用：

* **多臂吃角子老虎**：A [多臂吃角子老虎](https://en.wikipedia.org/wiki/Multi-armed_bandit){target="_blank"} 最佳化方法可在探索性學習與對該學習的利用之間取得平衡。

* **Thomson取樣**：Thompson取樣是線上決策問題的演演算法，其動作是循序漸進的，必須在挖掘已知最大即時效能與投資累積可能改善未來效能的新資訊之間取得平衡。 [了解详情](#thompson-sampling)

* [**Beta版分佈**](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}: Set of continuous [probability distributions](https://en.wikipedia.org/wiki/Probability_distribution){target="_blank"} defined on the interval [0, 1] [parameterized](https://en.wikipedia.org/wiki/Statistical_parameter){target="_blank"} by two positive [shape parameters](https://en.wikipedia.org/wiki/Shape_parameter){target="_blank"}.

## Thompson取樣 {#thompson-sampling}

自動最佳化的基礎演演算法是 **Thompson取樣**. 在本節中，我們將討論Thompson取樣背後的直覺。

[Thompson取樣](https://en.wikipedia.org/wiki/Thompson_sampling){target="_blank"}或稱為Bayesian bandit，是多臂吃角子老虎機問題的貝葉斯方法。  基本想法是將每個優惠的平均獎勵??視為一個 **隨機變數** 並使用我們目前所收集的資料來更新我們對於平均報酬的「信念」。 此「信念」在數學上以 **後驗概率分佈**  — 基本上是平均報酬的值範圍，以及每個優惠方案中報酬具有該值的可能性（或可能性）。 然後，對於每個決定，我們將 **從這些後驗回報分佈中取一個分數** 並選取抽樣報酬值最高的優惠方案。

下圖說明此程式，其中有3個不同的選件。 起初，我們無法從資料中取得任何證據，而且我們假設所有優惠方案都有一個統一的後驗回報分佈。 我們會從每個優惠方案的後獎勵分佈中抽取樣本。 從選件2的分佈中選取的範例具有最高值。 以下範例為 **探索**. 顯示選件2後，我們會收集任何潛在的獎勵（例如轉換/不轉換），並使用貝葉斯定理更新選件2的後驗分佈，如下所述。  我們繼續此程式，並在每次顯示優惠方案及收集獎勵時更新後續分配。 在第二個數字中，已選取Offer 3 — 儘管Offer 1具有最高的平均報酬（其後驗報酬分佈最靠右），從每個分佈取樣的程式已導致我們選擇明顯次優的Offer 3。 我們藉此機會，進一步瞭解Offer 3的真正回報分配。

當收集到更多樣本時，可信度會提高，而可能的獎勵會獲得更準確的預估（對應較窄的獎勵分佈）。 在有更多證據時更新我們信念的過程稱為 **貝葉斯推斷**.

最終，如果一個選件（例如選件1）是明確的贏家，其後驗回報分配將與其他選件分開。 此時，對於每個決定，從選件1抽樣所得的報酬可能是最高的，而我們將以較高的機率來選擇它。 這是 **開發**  — 我們堅信Offer 1是最佳選擇，因此選擇它是為了獲得最大回報。

![](../assets/ai-ranking-thompson-sampling.png)

**圖1**： *對於每項決定，我們都會從後驗回報分佈中取樣分數。 將會選擇具有最高範例值（轉換率）的選件。 在初始階段，所有選件都擁有統一的分佈方式，因為我們沒有任何證據可以證明資料中選件的轉換率。 當我們收集到更多樣本時，後驗分佈會變得更窄、更準確。 最終，每次都會選擇轉換率最高的選件。*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**技术详细信息**

若要計算/更新分配，我們使用 **Bayes定理**. 針對每個選件 ***i***，我們要計算其***P(??i |資料)***，即針對每個選件 ***i***，報酬值發生的機率為何 **??i** 是，根據我們目前為止為該選件收集的資料。

從Bayes定理：

***後驗概率=可能性*前驗概率***

此 **先驗概率** 是有關產生輸出機率的初始猜測。 收集到一些證據後的機率稱為 **後驗概率**. 

自動最佳化的設計會考量二進位獎勵（按一下/不按一下）。 在此案例中，可能性代表N個試驗中的成功數量，並由 **二項式分佈**. 對於某些似然函式，如果您選擇特定的前一個函式，後一個函式最終會處於與前一個函式相同的分佈中。 這樣的前置詞則稱為 **共軛驗前**. 這種先驗使後驗分佈的計算非常簡單。 此 **Beta版分佈** 是二項式可能性（二進位獎勵）之前的共軛值，因此對於前後概率分佈來說，是一種方便且合理的選擇。Beta分佈有兩個引數： ***α*** 和 ***β***. 這些引數可視為成功和失敗的計數，以及以下提供的平均值：

![](../assets/ai-ranking-beta-distribution.png)

如上所述的Likelihood函式由二項式分佈建模，具有s successful （轉換）和f failure （no — 轉換），而q是 [隨機變數](https://en.wikipedia.org/wiki/Random_variable){target="_blank"} with a [beta distribution](https://en.wikipedia.org/wiki/Beta_distribution){target="_blank"}.

前一個由Beta版分佈建模，後一個版分佈採用以下形式：

![](../assets/ai-ranking-posterior-distribution.svg)

計算後驗的方法為直接將成功和失敗數加到現有引數 ***α***， ***β***.

對於自動最佳化，如上述範例所示，我們以先前的分佈開始 ***Beta(1， 1)*** （均勻分佈）對於所有選件，在給定選件成功和失敗後，後驗會成為具有引數的Beta分佈 ***(s+α， f+β)*** 以取得該優惠方案。
+++

**相关主题**：

若要深入瞭解湯普森取樣，請閱讀下列研究檔案：
* [Thompson抽樣方法的實證評價](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target="_blank"}
* [多臂老虎機問題的Thompson抽樣分析](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target="_blank"}

## 冷啟動問題 {#cold-start}

當行銷活動新增新優惠方案，且沒有新優惠方案的轉換率相關資料時，就會出現「冷啟動」問題。 在此期間，我們必須提出一項策略，說明選擇此新選件的頻率，以便將效能下降降至最低，同時收集此新選件的轉換率相關資訊。 有多種解決方案可以解決這個問題。 關鍵是要在這項新優惠的探索之間找到平衡，同時我們又不會犧牲太多開發成果。 目前，我們使用「均勻分佈」作為新優惠方案轉換率（先前分佈）的初始猜測。 基本上，我們提供的所有轉換率值都等於發生的機率。


![](../assets/ai-ranking-cold-start-strategies.png)

**圖2**： *考慮包含3個選件的行銷活動。 在行銷活動上線時，選件4會新增至行銷活動。 我們最初沒有有關Offer 4轉換率的資料，因此必須處理冷啟動問題。 我們使用均勻分佈來作為我們對Offer 4轉換率的初步猜測，同時我們收集這個新選件的資料。 如 [Thompson取樣](#thompson-sampling) 區段，為了選擇將向使用者顯示哪個優惠方案，我們會從優惠方案的後驗獎勵分佈中取樣點，並選取具有最高取樣值的優惠方案。 在上述範例中，已選取Offer 4，稍後會根據所收集的獎勵，更新此優惠的後驗分佈，如 [Thompson取樣](#thompson-sampling) 區段。*

## 提升度測量 {#lift}

「提升度」量度可用來測量排名服務中部署的任何策略與基線策略（隨機提供選件）的效能。

例如，如果我們想要測量用於排名服務的湯普森取樣(TS)策略的效能，且KPI是轉換率(CVR)，則TS策略相對於基線策略的「提升度」定義為：

![](../assets/ai-ranking-lift.png)
