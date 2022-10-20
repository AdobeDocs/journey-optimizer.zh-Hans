---
title: 创建直邮
description: 了解如何在Journey Optimizer中创建直邮
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: e3ae60321aac340328e1fcd7b1060192fbc7ee06
workflow-type: tm+mt
source-wordcount: '856'
ht-degree: 3%

---

# 直邮配置 {#create-direct}

[!DNL Journey Optimizer] 允许您个性化并生成直邮提供商向客户发送邮件所需的文件。

准备直邮投放时， [!DNL Journey Optimizer] 会生成一个文件，其中包含所有定向的用户档案和所选的联系信息（例如邮政地址）。 然后，您可以将此文件发送给直邮提供商，由其负责发送纸质信函。

要发送直邮，您需要创建文件并将其上传到服务器。 要执行此操作，您需要先创建 [文件路由配置](#file-routing-configuration) 和 [直邮表面](#direct-mail-surface) 将引用文件路由配置。

## 配置文件路由 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="定义文件路由配置的设置"
>abstract="您需要定义将导出和上传文件的位置，以供直邮提供商使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="定义文件路由配置的设置"
>abstract="创建直邮时，将生成包含所有必需用户档案信息的文件。 需要将此文件导出并上传到服务器，以便您的直邮提供商可以访问并使用该文件传送直邮。"

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="文件路由配置"
>abstract="选择选择的文件路由配置，该配置定义将导出和上传文件的位置，以供直邮提供商使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="为文件路由选择服务器类型"
>abstract="选择要用于上传和存储直邮文件的服务器。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="选择AWS地区"
>abstract="选择要用于上传和存储直邮文件的服务器。 目前仅支持Amazon S3和SFTP。"

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 文件路由配置]** > **[!UICONTROL 文件路由]** 菜单，然后单击 **[!UICONTROL 创建路由配置]**.

   ![](assets/file-routing-config-button.png)

1. 设置配置的名称。

1. 选择配置 **[!UICONTROL 类型]**，即要用于上传和存储直邮文件的服务器。<!--why is it Type and not Server or Server type? asked to PM-->

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >目前，只有Amazon S3和SFTP可用。

   创建直邮时，将生成包含所有必需用户档案信息的文件。 需要将此文件导出并上传到服务器，以便您的直邮提供商可以访问并使用该文件传送直邮。

1. 填写特定于所选配置类型的详细信息和凭据，如服务器地址、访问密钥等。 <!--need to detail more?-->

   <!--![](assets/file-routing-config-aws-details.png)-->

   ![](assets/file-routing-config-sftp-details.png)

1. 如果已选择 **[!UICONTROL Amazon S3]**，则可以选择要导出和上传直邮文件的AWS区域。

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS地区是分布在世界各地的不同地理区域，AWS用这些区域来存放其基础设施。 为了获得最佳使用效果，建议选择最接近托管云基础架构的区域。

1. 选择 **[!UICONTROL 提交]**. 文件路由配置是使用 **[!UICONTROL 活动]** 状态。 现在，它可以用在直邮界面中，以便从 [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >您还可以选择 **[!UICONTROL 另存为草稿]** 创建文件路由配置，但在曲面上 **[!UICONTROL 活动]**.

## 创建直邮界面 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="定义直邮设置"
>abstract="直邮界面包含与包含直邮用户档案数据的文件格式相关的设置。 您可以（定义排序配置）、删除重复行、将记录拆分为多个文件并选择文件路由配置。"

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="定义排序顺序"
>abstract="如果选择此选项，则按配置文件ID（升序或降序）进行排序。 如果取消选择该消息，则在历程或营销策划中创建直邮时定义的排序配置。"

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="定义文件拆分阈值"
>abstract="必须为包含用户档案数据的每个文件设置最大记录数。 达到指定的阈值后，将为其余记录创建另一个文件。"

配置文件路由后，您需要创建一个渠道表面，以便能够从 [!DNL Journey Optimizer]. 在每个曲面中，需要选择文件路由配置。

1. 创建通道曲面。 [了解详情](channel-surfaces.md)

1. 选择 **[!UICONTROL 直邮]** 渠道。

   ![](assets/surface-direct-mail-channel.png)

1. 在渠道表面配置的专用部分中定义直邮设置。

   ![](assets/surface-direct-mail-settings.png)

1. 选择文件格式： **[!UICONTROL CSV]** 或 **[!UICONTROL 文本分隔]**.

1. 在 **[!UICONTROL 插入]** ，则可以选择自动删除重复的行。

1. 为包含用户档案数据的每个文件定义最大记录数（即行）。 达到指定的阈值后，将为其余记录创建另一个文件。

   ![](assets/surface-direct-mail-split.png)

   例如，如果文件中有100,000条记录，且阈值限制设置为60,000，则记录将被拆分为两个文件。 第一个文件将包含60,000行，第二个文件将包含其余40,000行。

   >[!NOTE]
   >
   >您可以设置介于1到200,000条记录之间的任意数字，这意味着每个文件必须至少包含1行且不超过200,000行。

1. 最后，选择 [文件路由配置](#file-routing-configuration) 在您创建的其中。 这可定义导出和上传文件的位置，以供直邮提供商使用。

   >[!CAUTION]
   >
   >如果未配置任何文件路由选项，则将无法创建直邮界面。 [了解详情](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)