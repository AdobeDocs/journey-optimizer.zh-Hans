---
title: 应用程序内渠道先决条件和配置
description: 了解如何配置环境以使用Journey Optimizer发送应用程序内消息
role: Admin
feature: In App
level: Intermediate
keywords: 应用程序内、消息、配置、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 21c15e003609a7ed016391bfe499ce245736db0e
workflow-type: tm+mt
source-wordcount: '819'
ht-degree: 10%

---

# 先决条件和配置 {#inapp-configuration}

能够在中发送应用程序内消息历程和营销活动 [!DNL Journey Optimizer]中，您需要完成以下配置步骤。

1. 在开始之前，请确保您对 Journey Optimizer 营销活动拥有适当的权限，即使您计划在历程中仅使用应用程序内消息。仍需要拥有营销活动权限。[了解详情](../campaigns/get-started-with-campaigns.md#campaign-prerequisites)
1. 在Adobe Experience Platform数据收集数据流中启用Adobe Journey Optimizer，并在Adobe Experience Platform中检查默认合并策略，如中所述 [投放先决条件](#delivery-prerequisites) 下。
1. 在Adobe Experience Platform数据收集中创建并配置应用程序表面，如中所述 [本节](#channel-prerequisites). 必须授予特定权限才能访问 **应用程序表面** Adobe Experience Platform数据收集中的菜单。 在[本视频](#video)中了解详情。
1. 如果您使用内容实验，请确保遵循中列出的要求 [本节](#experiment-prerequisite).

完成后，您可以创建、配置并发送您的第一条应用程序内消息。在[此部分](create-in-app.md)中了解如何实现这一点。


## 投放先决条件 {#delivery-prerequisites}

要正确投放应用程序内消息，必须定义以下设置：

* 在 [Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}，确保您有定义的数据流，例如 **[!UICONTROL Adobe Experience Platform]** 服务Adobe Experience Platform Edge和 **[!UICONTROL Adobe Journey Optimizer]** 选项已启用。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=zh-Hans){target="_blank"}

  ![](assets/inapp_config_6.png)

* 在 [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}, make sure you have the default merge policy with the **[!UICONTROL Active-On-Edge Merge Policy]** option enabled. To do this, select a policy under the **[!UICONTROL Customer]** > **[!UICONTROL Profiles]** > **[!UICONTROL Merge Policies]** Experience Platform menu. [Learn more](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  此合并策略的使用者为 [!DNL Journey Optimizer] 入站渠道，用于在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  >[!NOTE]
  >
  >使用自定义时 **[!UICONTROL 数据集偏好设置]** 合并策略，确保添加 **[!UICONTROL 入站历程]** 指定合并策略中的数据集。

  ![](assets/inapp_config_8.png)

## 渠道配置先决条件 {#channel-prerequisites}

1. 访问 **[!UICONTROL 应用程序表面]** 菜单并单击 **[!UICONTROL 创建应用程序表面]**.

1. 向添加名称 **[!UICONTROL 应用程序表面]**.

   ![](assets/inapp_config_2b.png)

1. 从 **[!UICONTROL Apple iOS]** 下拉框中，为Apple iOS配置移动应用程序。

+++ 了解详情

   1. 键入您的 **[!UICONTROL iOS包ID]**. 请参阅 [Apple文档](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) 有关的详细信息 **捆绑ID**.

   1. （可选）选择 **[!UICONTROL 沙盒]** 从中发送推送通知的位置。 请注意，选择特定的沙盒需要必要的访问权限。

      有关沙盒管理的更多信息，请参阅 [此页面](../administration/sandboxes.md#assign-sandboxes).

   1. 启用 **[!UICONTROL 推送凭据]** 选项，以根据需要拖放您的.p8身份验证密钥文件。

      您也可以启用 **[!UICONTROL 手动输入推送凭据]** 选项，用于直接复制和粘贴APNs身份验证密钥。

   1. 输入您的 **[!UICONTROL 密钥ID]** 和 **[!UICONTROL 团队编号]**.

      ![](assets/inapp_config_2.png)

+++

1. 从 **[!UICONTROL Android]** 下拉菜单中，为Android配置移动应用程序。

+++ 了解详情

   1. 键入您的 **[!UICONTROL Android包名称]**. 请参阅 [Android文档](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) 有关的详细信息 **包名称**.

   1. （可选）选择 **[!UICONTROL 沙盒]** 从中发送推送通知的位置。 请注意，选择特定的沙盒需要必要的访问权限。

      有关沙盒管理的更多信息，请参阅 [此页面](../administration/sandboxes.md#assign-sandboxes).

   1. 启用 **[!UICONTROL 推送凭据]** 选项，以根据需要拖放您的.json私钥文件。

      您也可以启用 **[!UICONTROL 手动输入推送凭据]** 用于直接复制和粘贴FCM私钥的选项。

      ![](assets/inapp_config_7.png)

1. 单击 **[!UICONTROL 保存]** 当您完成 **[!UICONTROL 应用程序表面]**.

   ![](assets/inapp_config_3.png)

   您的 **[!UICONTROL 应用程序表面]** 现在，在创建具有应用程序内消息的新促销活动时将可用。 [了解详情](create-in-app.md)

1. 创建应用程序表面后，您现在需要创建移动资产。

   请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) 以了解详细过程。

   ![](assets/inapp_config_4.png)

1. 从新创建资产的“扩展”菜单中，安装以下扩展：

   * Adobe Experience Platform边缘网络
   * Adobe Journey Optimizer
   * AEP保证
   * 同意
   * 标识
   * 移动核心
   * 配置文件

   请参阅 [此页面](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html#add-a-new-extension) 以了解详细过程。

   ![](assets/inapp_config_5.png)

应用程序内渠道现已配置。 您可以开始向用户发送应用程序内消息。

## 内容试验先决条件 {#experiment-prerequisites}

要为应用程序内渠道启用内容实验，您需要确保 [数据集](../data/get-started-datasets.md) 在应用程序内实施中使用 [数据流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"} 也包含在您的报表配置中。

换句话说，在配置试验报告时，如果添加的数据集不在Web数据流中，则Web数据将不会显示在内容试验报告中。

了解如何在中为内容实验报告添加数据集 [本节](../campaigns/reporting-configuration.md#add-datasets).

>[!NOTE]
>
>数据集由 [!DNL Journey Optimizer] 并且不影响数据收集或数据摄取。

如果您是 **非** 使用以下预定义的 [字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"} for your dataset schema: `AEP Web SDK ExperienceEvent` and `Consumer Experience Event` (as defined in [this page](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"})，确保添加以下字段组： `Experience Event - Proposition Interactions`， `Application Details`， `Commerce Details`、和 `Web Details`. 这些是必需的 [!DNL Journey Optimizer] 内容试验报告，并跟踪每个用户档案参与哪些试验和处理。

>[!NOTE]
>
>添加这些字段组不会影响正常数据收集。 它仅适用于正在运行试验的页面，而所有其他跟踪保持不变。

## 操作说明视频{#video}

以下视频介绍了如何分配 **管理应用程序配置** 访问“应用程序表面”菜单的权限。


>[!VIDEO](https://video.tv.adobe.com/v/3421607)


**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [设计应用程序内消息](design-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)

