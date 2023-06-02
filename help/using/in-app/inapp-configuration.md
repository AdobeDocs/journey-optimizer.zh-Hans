---
title: 应用程序内配置
description: 了解如何使用Journey Optimizer配置环境以发送应用程序内消息
role: Admin
level: Intermediate
keywords: 应用程序内、消息、配置、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 21aeac323a43ac95d98f4798ff3d51ad32f2ebf9
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 11%

---

# 配置应用程序内渠道 {#inapp-configuration}

在发送应用程序内消息之前，您需要在中配置应用程序内渠道 [!DNL Adobe Experience Platform Data Collection].

1. 来自您的 [!DNL Adobe Experience Platform Data Collection] 帐户，访问 **[!UICONTROL 数据流]** 菜单并单击 **[!UICONTROL 新建数据流]**. 有关创建数据流的详细信息，请参阅 [此页面](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. 选择 [!DNL Adobe Experience Platform] 服务。

   [!DNL Edge Segmentation] 和 [!DNL Adobe Journey Optimizer] 必须选中。

   ![](assets/inapp_config_6.png)

1. 然后，访问 **[!UICONTROL 应用程序表面]** 菜单，然后单击 **[!UICONTROL 创建应用程序表面]**.

   ![](assets/inapp_config_1.png)

1. 向添加名称 **[!UICONTROL 应用程序表面]**.

1. 从Apple iOS下拉列表中，键入 **iOS包ID**. 请参阅 [Apple文档](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 有关的详细信息 **捆绑包ID**.

   ![](assets/inapp_config_2.png)

1. 从Android下拉列表中，键入 **Android包名称**. 请参阅 [Android文档](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 有关的详细信息 **包名称**.

1. 单击 **[!UICONTROL 保存]** 完成配置时， **[!UICONTROL 应用程序表面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 应用程序表面]** 现在，在创建新的营销活动并显示应用程序内消息时，将可用。 [了解详情](create-in-app.md)

1. 创建应用程序表面后，您现在需要创建移动资产。

   请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 以了解详细过程。

   ![](assets/inapp_config_4.png)

1. 从新创建资产的“扩展”菜单中，安装以下扩展：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保证
   * 同意
   * 标识
   * 移动核心
   * 配置文件

   请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) 以了解详细过程。

   ![](assets/inapp_config_5.png)

应用程序内渠道现已配置。 您可以开始向用户发送应用程序内消息。

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [设计应用程序内消息](design-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
