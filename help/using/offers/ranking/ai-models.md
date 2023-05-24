---
product: experience platform
solution: Experience Platform
title: 開始使用AI模型
description: 瞭解允許對優惠進行排名的AI模型
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 4%

---

# 開始使用AI模型 {#ai-models}

[!DNL Journey Optimizer] 可讓您使用經過訓練的模型系統，對要針對指定設定檔顯示的選件進行排名。

此功能可讓您建立不同的 **AI模型** 根據您的業務目標而定。 在決定中使用這些不同的目標型策略，經過訓練的模型系統將幫助您瞭解不同的AI模型如何影響您的目標。

例如，您可以為電子郵件頻道選取一個AI模型，並為推播頻道選取另一個模型。 對於每個管道，經過訓練的模型系統將運用多個資料點來決定應先針對指定位置顯示哪個優惠，而不是考慮優惠的優先順序分數或 [排名公式](create-ranking-formulas.md).

## AI 模型类型 {#ai-model-types}

有兩種型別的AI模型可用於 [!DNL Journey Optimizer]：

* **自動最佳化模型** 旨在提供可大幅提升業務客戶設定之回報(KPI)的優惠方案。 這些KPI可以是轉換率、收入等形式。 此時，自動最佳化的重點是最佳化優惠點按，並將優惠轉換作為我們的目標。 自動最佳化是非個人化的，並根據選件的「全域」效能最佳化。 [了解详情](auto-optimization-model.md)

* **個人化模型** 可讓您定義業務目標，並利用客戶資料來訓練業務導向的模型，以提供個人化優惠方案並最大化KPI。 [了解详情](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >個人化最佳化模型目前僅供特定使用者提早存取。

## 建立AI模型 {#create-ai-model}

建立及使用AI模型的主要步驟如下：

1. 建立將收集轉換和曝光事件的資料集。 [了解详情](../data-collection/create-dataset.md)
1. 建立AI模型，運用資料集中的事件來排名選件。 [了解详情](create-ranking-strategies.md)
1. 設定您的優惠方案綱要以自動擷取事件。 [了解详情](../data-collection/schema-requirement.md)
1. 將AI模型指派給決定中的位置，以排名合格的優惠。 [了解详情](../offer-activities/configure-offer-selection.md)
