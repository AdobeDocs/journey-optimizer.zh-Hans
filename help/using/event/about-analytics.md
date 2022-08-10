---
title: 关于Adobe Analytics数据
description: 了解如何利用Adobe Analytics数据
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: 9d842722-e5eb-4743-849d-b7ba9448062f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 8%

---

# 利用Adobe Analytics数据{#analytics-data}

您可以利用已在捕获并流入到平台中的所有Adobe Analytics行为事件数据，以触发历程并自动化客户体验。

>[!NOTE]
>
>本节仅适用于基于规则的事件和需要使用Adobe Analytics数据的客户。

要使此功能正常工作，您需要在Adobe Experience Platform中激活要利用的报表包：

1. 在Adobe Experience Platform中，选择 **[!UICONTROL Sources]** then **[!UICONTROL Add data]** 在Adobe Analytics部分。 此时会显示可用的Adobe Analytics报表包列表。

1. 选择要启用的报表包，单击 **[!UICONTROL Next]** 单击 **[!UICONTROL Finish]**.

1. 与您的测试版计划联系人共享源数据ID。

这会为该报表包启用Analytics源连接器。 每当数据传入时，它都会转换为体验事件并发送到Adobe Experience Platform。

![](assets/jo-event9.png)

了解有关Adobe Analytics源连接器的更多信息，请参阅  [Adobe Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html?lang=zh-Hans){target=&quot;_blank&quot;}和 [教程](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html){target=&quot;_blank&quot;}。
