---
title: 应用程序内渠道先决条件和配置
description: 了解如何配置环境以使用Journey Optimizer发送应用程序内消息
role: Admin
feature: In App
level: Intermediate
keywords: 应用程序内、消息、配置、平台
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: d4dce7b31d898d86c330048e6d0a1587e87a617c
workflow-type: tm+mt
source-wordcount: '867'
ht-degree: 9%

---

# 先决条件和配置 {#inapp-configuration}

## 配置步骤 {#inapp-steps}

要在使用[!DNL Journey Optimizer]的历程和营销活动中发送应用程序内消息，您需要完成以下配置步骤。

1. 在开始之前，请确保您对 Journey Optimizer 营销活动拥有适当的权限，即使您计划在历程中仅使用应用程序内消息。仍需要拥有营销活动权限。[了解详情](../campaigns/get-started-with-campaigns.md#campaign-prerequisites)。
1. 在Adobe Experience Platform数据收集数据流中启用Adobe Journey Optimizer，并检查Adobe Experience Platform中的默认合并策略，如下面的[交付先决条件](#delivery-prerequisites)中所述。
1. 在“管理”>“渠道”>“渠道配置”中创建应用程序内消息渠道配置，如[此部分](#channel-prerequisites)所述。
1. 如果您使用内容实验，请确保遵循[此部分](#experiment-prerequisite)中列出的要求。

完成后，您可以创建、配置并发送您的第一条应用程序内消息。在[此部分](create-in-app.md)中了解如何实现这一点。

## 投放先决条件 {#delivery-prerequisites}

要正确投放应用程序内消息，必须定义以下设置：

* 在[Adobe Experience Platform数据收集](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=zh-Hans){target="_blank"}中，确保您已定义数据流，例如在&#x200B;**[!UICONTROL Adobe Experience Platform]**&#x200B;服务下，您已启用Adobe Experience Platform Edge和&#x200B;**[!UICONTROL Adobe Journey Optimizer]**&#x200B;选项。

  这可确保Adobe Experience Platform Edge正确处理Journey Optimizer入站事件。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html){target="_blank"}

  ![](assets/inapp_config_6.png)

* 在[Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中，确保您已启用默认合并策略&#x200B;**[!UICONTROL Active-On-Edge合并策略]**&#x200B;选项。 为此，请在&#x200B;**[!UICONTROL 客户]** > **[!UICONTROL 配置文件]** > **[!UICONTROL 合并策略]**&#x200B;策略菜单下选择Experience Platform。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html#configure){target="_blank"}

  [!DNL Journey Optimizer]入站渠道使用此合并策略在边缘上正确激活和发布入站营销活动。 [了解详情](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=zh-Hans){target="_blank"}

  >[!NOTE]
  >
  >使用自定义&#x200B;**[!UICONTROL 数据集偏好设置]**&#x200B;合并策略时，请确保在指定的合并策略中添加&#x200B;**[!UICONTROL 历程入站]**&#x200B;数据集。

  ![](assets/inapp_config_8.png)

* 要对Journey Optimizer移动体验的交付进行故障诊断，您可以使用&#x200B;**Edge Delivery保证**&#x200B;中的&#x200B;**Adobe Experience Platform**&#x200B;视图。 利用此插件，您可以详细检查请求调用，验证预期的边缘调用是否按预期发生，并检查配置文件数据，包括身份映射、区段成员资格和同意设置。 此外，您还可以查看请求符合条件的活动，并识别未符合条件的活动。

  使用&#x200B;**Edge Delivery**&#x200B;插件可帮助您获得所需的见解，以便有效了解入站实施并排除其故障。

  [了解有关Edge Delivery视图的更多信息](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/assurance/view/edge-delivery)

## 创建应用程序内配置 {#channel-prerequisites}

1. 访问&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 常规设置]** > **[!UICONTROL 渠道配置]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。

   ![](assets/inapp_config_1.png)

1. 输入配置的名称和说明（可选），然后选择要配置的渠道。

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您还可以使用下划线`_`、点`.`和连字符`-`字符。

1. 要为配置分配自定义或核心数据使用标签，您可以选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解有关对象级访问控制(OLAC)的更多信息](../administration/object-based-access.md)。

1. 选择&#x200B;**[!UICONTROL 营销操作]**&#x200B;以使用此配置将同意策略关联到消息。 所有与营销活动相关的同意政策均可利用，以尊重客户的偏好。 [了解详情](../action/consent.md#surface-marketing-actions)

1. 选择&#x200B;**应用程序内消息传送**&#x200B;渠道。

   ![](assets/inapp_config_9.png)

1. 选择要应用应用程序内消息的平台。

   ![](assets/inapp_config_10.png)

1. 对于Web：

   * 您可以输入&#x200B;**[!UICONTROL 页面URL]**&#x200B;以将更改应用于特定页面。

   * 您可以创建一个规则来定位遵循相同模式的多个URL。

+++ 如何构建页面匹配规则。

      1. 选择&#x200B;**[!UICONTROL 页面匹配规则]**&#x200B;作为应用程序配置，并输入您的&#x200B;**[!UICONTROL 页面URL]**。

      1. 在&#x200B;**[!UICONTROL 编辑配置规则]**&#x200B;窗口中，为&#x200B;**[!UICONTROL 域]**&#x200B;和&#x200B;**[!UICONTROL 页面]**&#x200B;字段定义条件。
      1. 从“条件”下拉列表中，进一步将您的条件个性化。

         例如，在本例中，要编辑显示在Luma网站所有销售产品页面上的元素，请选择域>开头为> Luma和页面>包含>销售。

         ![](assets/in_app_web_surface_4.png)

      1. 如果需要，单击&#x200B;**[!UICONTROL 添加其他页面规则]**&#x200B;以创建其他规则。

      1. 选择&#x200B;**[!UICONTROL 默认创作和预览URL]**。

      1. 保存您的更改。该规则显示在&#x200B;**[!UICONTROL 创建营销活动]**&#x200B;屏幕中。

+++

1. 对于iOS和Android：

   * 输入您的&#x200B;**[!UICONTROL 应用程序ID]**。

1. 提交更改。

现在，您可以在创建应用程序内消息时选择配置。

## 报告先决条件 {#experiment-prerequisites}

>[!NOTE]
>
>该数据集由[!DNL Journey Optimizer]报表系统以只读方式使用，不影响数据收集或数据摄取。

要为应用程序内渠道启用报表，您需要确保应用程序内实施[数据流](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html){target="_blank"}中使用的[数据集](../data/get-started-datasets.md)也包含在报表配置中。

换言之，在配置报表时，如果添加的数据集不在应用程序数据流中，则应用程序数据将不会显示在报表中。

在[本节](../reports/reporting-configuration.md#add-datasets)中了解如何添加用于报告的数据集。

如果您&#x200B;**不是**，正在为数据集架构使用以下预定义的[字段组](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=zh_Hans#field-group){target="_blank"}： `AEP Web SDK ExperienceEvent`和`Consumer Experience Event`（如[此页面](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas.html#add-field-groups){target="_blank"}中定义），请确保添加以下字段组： `Experience Event - Proposition Interactions`、`Application Details`、`Commerce Details`和`Web Details`。 [!DNL Journey Optimizer]内容试验报告需要这些项，因为它们正在跟踪每个配置文件参与哪些试验和处理。

[了解有关报告配置的更多信息](../reports/reporting-configuration.md)

>[!NOTE]
>
>添加这些字段组不会影响正常数据收集。 它仅适用于正在运行试验的页面，而所有其他跟踪保持不变。

**相关主题：**

* [创建应用程序内消息](create-in-app.md)
* [创建营销活动](../campaigns/create-campaign.md)
* [设计应用程序内消息](design-in-app.md)
* [应用程序内报告](../reports/campaign-global-report.md#inapp-report)

