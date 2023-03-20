---
title: 直邮配置
description: 了解如何在Journey Optimizer中配置直邮渠道
feature: Overview
topic: Content Management
role: User
level: Beginner
keyword: direct, mail, configuration, direct-mail, provider
hide: true
hidefromtoc: true
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
badge: label="Beta" type="Informitive"
source-git-commit: 55f1c6a681aece6446a3330184466ff61e4db580
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 1%

---

# 直邮配置 {#direct-mail-configuration}

>[!BEGINSHADEBOX]

您将在本文档中找到的内容：

* [创建直邮](create-direct-mail.md)
* **[配置直邮](direct-mail-configuration.md)**

>[!ENDSHADEBOX]

[!DNL Journey Optimizer] 允许您个性化并生成直邮提供商向客户发送邮件所需的文件。

When [创建直邮](../direct-mail/create-direct-mail.md)，则可定义目标受众数据，包括所选的联系信息（例如邮政地址）。 然后，将自动生成包含此数据的文件并将其导出到服务器，您的直邮提供商将能够在其中检索该文件并处理实际发送。

在能够生成此文件之前，您需要创建：

1. A [文件路由配置](#file-routing-configuration) 指定将导出文件的服务器。

1. A [直邮表面](#direct-mail-surface) 将引用文件路由配置。

>[!CAUTION]
>
>如果未配置任何文件路由选项，则将无法创建直邮界面。

## 配置文件路由 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="定义文件路由配置"
>abstract="创建直邮后，将生成包含目标受众数据的文件并将其导出到服务器。 您需要指定服务器详细信息，以便您的直邮提供商可以访问并使用该文件来传送直邮。"

<!--
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html" text="Create a direct mail message"-->

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="定义文件路由配置"
>abstract="您需要定义将文件导出到何处，以供直邮提供商使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="文件路由配置"
>abstract="选择选择的文件路由配置，该配置定义将导出文件以供直邮提供商使用的位置。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="为文件选择服务器类型"
>abstract="选择要用于导出直邮文件的服务器类型。 目前，Journey Optimizer仅支持Amazon S3和SFTP。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="选择AWS地区"
>abstract="选择要导出直邮文件的AWS服务器的地理区域。 通常情况下，最好选择与直邮提供商所在位置最接近的区域。"

要发送直邮， [!DNL Journey Optimizer] 生成包含目标受众数据的文件并将其导出到服务器。

您需要指定服务器详细信息，以便您的直邮提供商可以访问并使用该文件来传送邮件。

要配置文件路由，请执行以下步骤。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 文件路由配置]** > **[!UICONTROL 文件路由]** 菜单，然后单击 **[!UICONTROL 创建路由配置]**.

   ![](assets/file-routing-config-button.png)

1. 设置配置的名称。

1. 选择 **[!UICONTROL 服务器类型]** 用于导出直邮文件的URL。

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >目前，仅Amazon S3和SFTP在 [!DNL Journey Optimizer].

1. 填写服务器的详细信息和凭据，如服务器地址、访问密钥等。

   ![](assets/file-routing-config-sftp-details.png)

1. 如果已选择 **[!UICONTROL Amazon S3]**，选择 **[!UICONTROL AWS地区]** 服务器基础架构的位置。

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >AWS地区是AWS用来托管其云基础架构的地理区域。 通常情况下，最好选择与直邮提供商位置最接近的区域。

1. 选择&#x200B;**[!UICONTROL 提交]**。文件路由配置是使用 **[!UICONTROL 活动]** 状态。 现在，它已准备好用于 [直邮表面](#direct-mail-surface).

   >[!NOTE]
   >
   >您还可以选择 **[!UICONTROL 另存为草稿]** 创建文件路由配置，但在曲面上 **[!UICONTROL 活动]**.

## 创建直邮界面 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="定义直邮设置"
>abstract="直邮界面包含文件格式设置，其中包含目标受众数据，将由邮件提供商使用。 您还必须通过选择文件路由配置来定义将导出文件的位置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html?lang=en#file-routing-configuration" text="配置文件路由"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="定义文件拆分阈值"
>abstract="您必须为包含受众数据的每个文件设置最大记录数。 您可以选择介于1到200,000条记录之间的任意数字。 达到指定的阈值后，将为其余记录创建另一个文件。"

能够通过 [!DNL Journey Optimizer]，则需要创建渠道表面以定义将由邮件提供商使用的文件格式的设置。

直邮界面还必须包括文件路由配置，该配置定义了将导出直邮文件的服务器。

1. 创建通道曲面。 [了解详情](../configuration/channel-surfaces.md)

1. 选择 **[!UICONTROL 直邮]** 渠道。

   ![](assets/surface-direct-mail-channel.png)

1. 在渠道表面配置的专用部分中定义直邮设置。

   ![](assets/surface-direct-mail-settings.png)

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. 选择文件格式： **[!UICONTROL CSV]** 或 **[!UICONTROL 文本分隔]**.

1. 选择 **[!UICONTROL 文件路由配置]** 在您创建的其中。 这定义了将文件导出到何处以供直邮提供商使用。

   >[!CAUTION]
   >
   >如果未配置任何文件路由选项，则将无法创建直邮界面。 [了解详情](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. 提交直邮表面。

您现在可以 [创建直邮](../direct-mail/create-direct-mail.md) 在营销策划中。 营销活动启动后，包含目标受众数据的文件将自动导出到您定义的服务器。 然后，直邮提供商将能够检索该文件并继续直邮投放。

>[!NOTE]
>
>将自动删除重复的行。
>
>如果每个包含用户档案数据的文件的最大记录数（即行数）过高，将自动为其余记录创建另一个文件。

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->