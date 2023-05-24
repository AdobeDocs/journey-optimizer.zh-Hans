---
solution: Journey Optimizer
product: journey optimizer
title: 关于事件
description: 了解事件
feature: Events
topic: Administration
role: Admin
level: Intermediate
keywords: 事件，事件，歷程，定義，開始
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '980'
ht-degree: 63%

---

# 关于事件{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="关于事件"
>abstract="事件与个人相关联。它与个人的行为有关（例如，某人购买了产品、访问了商店、退出了网站等）或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是 Journey Optimizer 在历程中将侦听的内容，以编排最佳的后续行动。"

事件配置允许您定义 [!DNL Journey Optimizer] 将作为事件接收的信息。您可以使用多个事件（在历程的不同步骤中），而多个历程可以使用相同的事件。

>[!CAUTION]
>
>事件設定為 **強制** 而且必須由 **資料工程師**.

您可以設定兩種事件：

* **單一** 事件：這些事件會連結至人員。 它與人的行為相關（例如，某人購買產品、造訪商店、離開網站等） 或者与个人相关的某件事情有关（例如，某人达到 10 000 个忠诚点）。这就是 [!DNL Journey Optimizer] 在历程中将侦听的内容，以编排最佳的后续行动。單一事件可以是規則型或系統產生。 若要瞭解如何建立單一事件，請參閱此 [頁面](../event/about-creating.md).

* **企業** 事件：與單一事件相反，商業事件是指未連結至特定設定檔的事件。 例如，可以是新聞警報、運動更新、航班變更或取消、詳細目錄更新、天氣事件等。 雖然這些事件不是設定檔特有，但任何數量的設定檔都可能有興趣：訂閱特定新聞主題的個人、航班上的乘客、對無存貨產品感興趣的購物者等。 業務事件一律以規則為基礎。 當您將業務事件拖放到歷程中時，它會自動新增 **讀取區段** 活動緊接在後。 若要瞭解如何建立商業活動，請參閱此 [頁面](../event/about-creating-business.md).


>[!NOTE]
>
>如果您编辑在草稿或实时历程中使用的事件，则只能更改名称、描述或添加有效负载字段。我们严格限制草稿或实时历程的版本，以避免中断历程。

单一历程（以事件或区段资格开始）包含护栏，可防止同一事件多次错误触发历程。默认情况下，重新访问用户档案会被暂时阻止 5 分钟。例如，如果某个事件在 12:01 触发某个特定用户档案的历程，而另一个事件在 12:03 到达（无论是同一事件还是其他事件触发同一历程），则对于此用户档案，该历程将不会重新开始。

➡️ [在视频中发现此功能](#video)

## 事件ID型別{#event-id-type}

對於業務事件，事件ID型別一律以規則為基礎。

單一事件有兩種事件ID：

* **基于规则**&#x200B;的事件：此类型的事件不生成 eventID。使用简单表达式编辑器，您只需定义规则即可，系统将使用该规则来识别将触发历程的相关事件。此规则可以基于事件有效负荷中可用的任何字段，例如用户档案的位置或添加到用户档案购物车的项目数。

   >[!CAUTION]
   >
   >为基于规则的事件定义上限规则。對於指定的組織，歷程可處理的合格事件數限製為每秒5000。 它對應於Journey Optimizer SLA。 請參閱您的Journey Optimizer授權和 [Journey Optimizer產品說明](https://helpx.adobe.com/cn/legal/product-descriptions/adobe-journey-optimizer.html).

* **系统生成**&#x200B;的事件：这些事件需要 eventID。创建事件时会自动生成此 eventID 字段。推送事件的系统不应生成 ID，它应传递有效负荷预览中可用的 ID。

>[!NOTE]
>
>Journey Optimizer 要求将事件流式传输到数据收集核心服务 (DCCS) 才能触发历程。批量摄取的事件或来自内部 Journey Optimizer 数据集（消息反馈、电子邮件跟踪等）的事件无法用于触发历程。对于无法获取流式传输的事件的用例，请基于这些事件构建一个区段，然后改用&#x200B;**读取区段**&#x200B;活动。从技术上讲，可以使用区段鉴别，但根据所使用的操作，可能会导致下游挑战。此数据不一定需要转至实时用户档案。如果要在单独的历程中使用事件进行分段或查找，我们建议您为用户档案启用数据集。

## 数据周期 {#data-cycle}

事件是 POST API 调用。事件會透過串流獲取API傳送至Adobe Experience Platform。 通过事务性消息传送 API 发送的事件的 URL 目标称为“入口”。事件的有效负载遵循 XDM 格式。

有效負載包含串流獲取API運作（在標題中）所需的資訊，以及所需的資訊 [!DNL Journey Optimizer] 用於工作和用於歷程的資訊（在正文中，例如放棄購物車的金額）。 流式引入有两种模式，即验证和未验证。有关流式引入 API 的详细信息，请参阅[此链接](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=zh-Hans)。

在透過串流獲取API到達目的地之後，事件會流入名為Pipeline的內部服務，再流入Adobe Experience Platform。 如果事件架构启用了实时客户资料服务标志，并且数据集 ID 也具有实时客户资料标志，则会流入实时客户资料服务。

對於系統產生的事件，Pipeline會篩選其裝載包含下列內容的事件 [!DNL Journey Optimizer] eventIDs （請參閱下方的事件建立程式），由 [!DNL Journey Optimizer] 和包含在事件裝載中。 對於規則型事件，系統會使用eventID條件來識別事件。 这些事件通过 [!DNL Journey Optimizer] 侦听，并触发相应的旅程。

## 操作说明视频 {#video}

了解如何配置事件、指定流媒体端点和事件的有效负载。

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

了解商业事件的适用用例。 了解如何使用商业事件构建历程以及可以应用的最佳实践。

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
