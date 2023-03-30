---
title: 应用程序内配置
description: 了解如何配置环境以使用Journey Optimizer发送应用程序内消息
role: Admin
level: Intermediate
keywords: 应用程序内，消息，配置，平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: e35aeba17f45145cc7712740cbcf1f0e169760fc
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 11%

---

# 配置应用程序内渠道 {#inapp-configuration}

在发送应用程序内消息之前，您需要在 [!DNL Adobe Experience Platform Data Collection].

1. 从 [!DNL Adobe Experience Platform Data Collection] 帐户，访问 **[!UICONTROL 数据流]** 菜单，单击 **[!UICONTROL 新数据流]**. 有关数据流创建的更多信息，请参阅 [本页](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. 选择 [!DNL Adobe Experience Platform] 服务。

   [!DNL Edge Segmentation] 和 [!DNL Adobe Journey Optimizer] 必须被选中。

   ![](assets/inapp_config_6.png)

1. 然后，访问 **[!UICONTROL 应用程序曲面]** 菜单，然后单击 **[!UICONTROL 创建应用程序曲面]**.

   ![](assets/inapp_config_1.png)

1. 向 **[!UICONTROL 应用程序界面]**.

1. 从Apple iOS下拉菜单中，键入 **iOS包ID**. 请参阅 [Apple文档](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 有关 **包ID**.

   ![](assets/inapp_config_2.png)

1. 从Android下拉菜单中，键入 **Android包名称**. 请参阅 [Android文档](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 有关 **包名称**.

1. 单击 **[!UICONTROL 保存]** 完成 **[!UICONTROL 应用程序界面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 应用程序界面]** 现在，在使用应用程序内消息创建新营销活动时，将可用。 [了解详情](create-in-app.md)

1. 现在，创建应用程序界面后，您需要创建移动资产。

   请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 详细程序。

   ![](assets/inapp_config_4.png)

1. 从新创建资产的Extensions菜单中，安装以下扩展：

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * AEP保证
   * 同意
   * 识别
   * 移动核心
   * 配置文件

   请参阅 [本页](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) 详细程序。

   ![](assets/inapp_config_5.png)

应用程序内渠道现已配置完成。 您可以开始向用户发送应用程序内消息。

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [设计应用程序内消息](design-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)
