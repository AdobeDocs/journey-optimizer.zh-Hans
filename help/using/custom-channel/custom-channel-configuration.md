---
title: 为自定义渠道创建渠道配置
description: 了解如何在Adobe Journey Optimizer中为自定义渠道创建渠道配置。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限发布版" type="Informative"
source-git-commit: 9dfa2792db981f5f1a4e9fc3868ffd200c855a5b
workflow-type: tm+mt
source-wordcount: '383'
ht-degree: 8%

---


# 创建渠道配置 {#create-channel-config}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在Adobe Journey Optimizer中为自定义渠道创建渠道配置，并将其链接到API凭据、可选子域和有效负载默认值，以便营销人员在构建营销活动和历程时可以选择它。

>[!ENDSHADEBOX]

渠道配置将您的自定义渠道链接到营销人员在构建营销活动和历程时选择的已命名的可重用预设。

要为自定义渠道创建渠道配置，请执行以下步骤。

1. 转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 渠道配置]**，然后单击&#x200B;**[!UICONTROL 创建渠道配置]**。 了解有关[创建渠道配置](../configuration/channel-surfaces.md)的更多信息。

1. 从&#x200B;**[!UICONTROL 选择渠道]**&#x200B;下拉列表中，选择一个已激活的自定义渠道。

   ![选择频道](assets/custom_channel_select_channel.png){width="100%"}

1. 如果所选渠道使用身份验证（类型不是&#x200B;**无**），则显示&#x200B;**[!UICONTROL API凭据]**&#x200B;字段。 选择要用于此配置的凭据。 [了解有关API凭据的更多信息](custom-channel-api-credentials.md)

   ![选择API凭据](assets/custom_channel_config_api_credentials.png){width="100%"}

1. 如果您在[!DNL Journey Optimizer]中为自定义渠道设置了子域，则可以选择一个已委派的子域，以用于跟踪此配置的有效负载中存在的链接。 [了解如何委派子域](custom-channel-subdomains.md)

1. 如果所选渠道具有定义为端点URL的变量](create-custom-channel.md#endpoint-configuration)的标头或查询参数[，则会显示&#x200B;**[!UICONTROL 动态参数]**&#x200B;部分。

   输入每个参数的值。 您可以使用个性化编辑器插入动态值（例如，从用户档案解析的用户标识符）。 这样，您就可以根据每个收件人的配置文件数据为其自定义请求。

   ![动态参数](assets/custom_channel_config_dynamic_parameters.png){width="100%"}

1. 如果自定义渠道的有效负载字段启用了&#x200B;**[!UICONTROL 渠道配置]**&#x200B;复选框，则这些字段会显示在&#x200B;**[!UICONTROL 有效负载配置]**&#x200B;部分。 [了解详情](create-custom-channel.md#payload-configuration)

   ![有效负载字段](assets/custom_channel_config_payload.png){width="100%"}

   为此配置相应地为每个字段配置一个值。 这对于那些可能因营销活动或历程的上下文而不同的字段非常有用，例如发件人信息或消息模板。

1. 对于编排的营销活动，请完成&#x200B;**[!UICONTROL 执行详细信息]**&#x200B;部分以映射配置文件维度并指定执行地址。

   ![编排的营销活动中的执行详细信息](assets/custom_channel_oc_execution_details.png){width="80%"}

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;保存并激活渠道配置。

<!--
>[!CAUTION]
>
>If your organization uses approval policies, you may need to request approval before activating journeys or campaigns that use this channel configuration. [Learn more](../test-approve/gs-approval.md)
-->

## 后续步骤 {#next-steps}

您的自定义渠道现已完全配置。 营销人员可以开始使用此插件构建客户体验：

* [创建自定义渠道体验](create-custom-experience.md)
* [测试您的自定义渠道](test-custom-channel.md)
* [监测自定义渠道](configure-custom-channel.md)
