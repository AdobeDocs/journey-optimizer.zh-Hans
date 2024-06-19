---
title: 直邮配置
description: 了解如何在Journey Optimizer中配置直邮渠道
feature: Direct Mail, Surface
topic: Content Management
role: User
level: Experienced
keyword: direct, mail, configuration, direct-mail, provider
exl-id: ae5cc885-ade1-4683-b97e-eda1f2142041
source-git-commit: c7d8dd94bde49e8d02fe553fbac3942f55bf73fe
workflow-type: tm+mt
source-wordcount: '1272'
ht-degree: 22%

---

# 直邮配置 {#direct-mail-configuration}

[!DNL Journey Optimizer] 允许您个性化并生成直邮提供商向客户发送邮件所需的文件。

时间 [创建直邮消息](../direct-mail/create-direct-mail.md)，您可以定义目标受众数据，包括选定的联系信息（例如邮政地址）。 然后，包含此数据的文件将自动生成并导出到服务器，您的直邮提供商将能够检索它并处理实际发送。

在生成此文件之前，您需要创建：

1. A [文件路由配置](#file-routing-configuration) 指定要导出文件的服务器并加密文件（如有必要）。

   >[!CAUTION]
   >
   >要创建文件路由配置，您需要具有 **[!DNL Manage file routing]** 内置权限。 [了解详情](../administration/ootb-product-profiles.md#content-library-manager)。

1. A [直邮表面](#direct-mail-surface) 将引用文件路由配置。 如果尚未配置任何文件路由选项，您将无法创建直邮表面。

## 配置文件路由 {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="定义文件路由配置"
>abstract="创建直邮之后，将生成包含目标受众数据的文件并将其导出到服务器。您需要指定服务器详细信息，以便直邮提供商访问并使用该文件来投递直邮。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/create-direct-mail.html?lang=zh-Hans" text="创建直邮消息"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="定义文件路由配置"
>abstract="您需要定义将文件导出到何处以供直邮提供商使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="文件路由配置"
>abstract="选择您要使用的文件路由配置，这会定义将文件导出到何处以供您的直邮提供商使用。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="为文件选择服务器类型"
>abstract="选择您在导出直邮文件时要使用的服务器类型。Journey Optimizer 目前仅支持 Amazon S3 和 SFTP。"

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="选择 AWS 区域"
>abstract="选择要将直邮文件导出到的 AWS 服务器的地理区域。作为常规做法，最好选择离您的直邮提供商位置最近的区域。"

>[!NOTE]
>
>目前，支持Amazon S3、SFTP和Azure [!DNL Journey Optimizer].

要发送直邮消息， [!DNL Journey Optimizer] 生成包含目标受众数据的文件并将其导出到服务器。

您需要指定服务器详细信息，以便直邮提供商能够访问并使用该文件传递邮件。

要配置文件路由，请执行以下步骤。

>[!BEGINTABS]

>[!TAB Amazon S3]

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 文件路由配置]** > **[!UICONTROL 文件路由]** 菜单，然后单击 **[!UICONTROL 创建路由配置]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. 为您的配置设置一个名称。

1. 选择 **Amazon S3** 作为 **[!UICONTROL 服务器类型]** 用于导出直邮文件。

   ![](assets/file-routing-config-type.png){width="800" align="center"}

1. 填写服务器的详细信息和凭据

   * **AWS存储段名称**：要了解在何处查找您的AWS存储段名称，请参阅 [此页面](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html).

   * **AWS访问密钥**：要了解在何处查找您的AWS访问密钥ID，请参阅 [此页面](https://docs.aws.amazon.com/IAM/latest/UserGuide/security-creds.html#access-keys-and-secret-access-keys).

   * **AWS密钥**：要了解在何处查找您的AWS密钥，请参阅 [此页面](https://aws.amazon.com/fr/blogs/security/wheres-my-secret-access-key/).

   * **AWS地区**：选择 **[!UICONTROL AWS地区]** 服务器基础架构所在的位置。 AWS区域是AWS用来托管其云基础架构的地理区域。 通常，最好选择距离直邮提供商所在位置最近的区域。

   ![](assets/file-routing-config-aws-region.png){width="800" align="center"}

1. 要加密文件，请将加密密钥复制并粘贴到 **[!UICONTROL PGP/GPG加密密钥]** 字段。

1. 选择 **[!UICONTROL 提交]**. 文件路由配置是使用 **[!UICONTROL 活动]** 状态。 它现在已准备好用于 [直邮表面](#direct-mail-surface).

   您还可以选择 **[!UICONTROL 另存为草稿]** 创建文件布线配置，但在曲面中选取它之前，您将无法选取它 **[!UICONTROL 活动]**.

>[!TAB SFTP]

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 文件路由配置]** > **[!UICONTROL 文件路由]** 菜单，然后单击 **[!UICONTROL 创建路由配置]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. 为您的配置设置一个名称。

1. 选择SFTP作为 **[!UICONTROL 服务器类型]** 用于导出直邮文件。

   ![](assets/file-routing-config-type-sftp.png){width="800" align="center"}

1. 填写服务器的详细信息和凭据：

   * **帐户**：用于连接到SFTP服务器的帐户名称。

   * **服务器地址**：SFTP服务器的&#x200B;URL。

   * **端口**：FTP连接端口号。

   * **密码**：&#x200B;用于连接到SFTP服务器的密码。

   ![](assets/file-routing-config-sftp-detail.png)

1. 要加密文件，请将加密密钥复制并粘贴到 **[!UICONTROL PGP/GPG加密密钥]** 字段。

1. 选择 **[!UICONTROL 提交]**. 文件路由配置是使用 **[!UICONTROL 活动]** 状态。 它现在已准备好用于 [直邮表面](#direct-mail-surface).

   您还可以选择 **[!UICONTROL 另存为草稿]** 创建文件布线配置，但在曲面中选取它之前，您将无法选取它 **[!UICONTROL 活动]**.

>[!TAB Azure]

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 文件路由配置]** > **[!UICONTROL 文件路由]** 菜单，然后单击 **[!UICONTROL 创建路由配置]**.

   ![](assets/file-routing-config-button.png){width="800" align="center"}

1. 为您的配置设置一个名称。

1. 选择Azure **[!UICONTROL 服务器类型]** 用于导出直邮文件。

   ![](assets/file-routing-config-type-azure.png){width="800" align="center"}

1. 填写服务器的详细信息和凭据：

   * **Azure连接字符串**：查找您的 **Azure连接字符串**，请参阅 [此页面](https://learn.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string#configure-a-connection-string-for-an-azure-storage-account).

     此 **Azure连接字符串** 应遵循以下格式：

     `DefaultEndpointsProtocol=[http|https];AccountName=myAccountName;AccountKey=myAccountKey`

   * **容器名称**：查找您的 **容器名称**，请参阅 [此页面](https://learn.microsoft.com/en-us/azure/storage/blobs/blob-containers-portal).

     此 **容器名称** 应仅包含容器名称，且不含任何斜杠。 要在容器中指定保存文件的路径，请更新直邮营销活动的文件名以包含所需的路径。

1. 要加密文件，请将加密密钥复制并粘贴到 **[!UICONTROL PGP/GPG加密密钥]** 字段。

1. 选择 **[!UICONTROL 提交]**. 文件路由配置是使用 **[!UICONTROL 活动]** 状态。 它现在已准备好用于 [直邮表面](#direct-mail-surface).

   您还可以选择 **[!UICONTROL 另存为草稿]** 创建文件布线配置，但在曲面中选取它之前，您将无法选取它 **[!UICONTROL 活动]**.

>[!ENDTABS]

## 创建直邮表面 {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="定义直邮设置"
>abstract="直邮表面包含文件的格式设置，文件中包含目标受众数据，将由邮件提供商使用。您还必须选择文件路由配置来定义文件的导出位置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/direct-mail/direct-mail-configuration.html?lang=zh-Hans#file-routing-configuration" text="配置文件路由"

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="定义文件拆分阈值"
>abstract="您必须为包含受众数据的每个文件设置最大记录数。您可以选择 1 到 200,000 之间的任意记录数。达到指定阈值后，将创建另一个文件用于其余的记录。"

能够发送直邮 [!DNL Journey Optimizer]，则需要创建渠道表面来定义邮件提供商使用的文件格式设置。

直邮表面还必须包括文件路由配置，该配置定义了将导出直邮文件的服务器。

1. 创建渠道表面。 [了解详情](../configuration/channel-surfaces.md)

1. 选择 **[!UICONTROL 直邮]** 渠道。

   ![](assets/surface-direct-mail-channel.png){width="800" align="center"}

1. 在渠道平面配置的专用部分中定义直邮设置。

   ![](assets/surface-direct-mail-settings.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-settings-with-insertion.png)-->

1. 选择文件格式： **[!UICONTROL CSV]** 或 **[!UICONTROL 文本分隔]**.

1. 如果您选择 **[!UICONTROL 文本分隔]**，定义所选的列分隔符：制表、分号、竖线或&amp;符号。

   ![](assets/surface-direct-mail-column-separator.png)

1. 选择 **[!UICONTROL 文件路由配置]** 在您创建的那些报表中。 这会定义文件的导出位置，以供直邮提供商使用。

   >[!CAUTION]
   >
   >如果尚未配置任何文件路由选项，您将无法创建直邮表面。 [了解详情](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png){width="800" align="center"}

   <!--![](assets/surface-direct-mail-file-routing-with-insertion.png)-->

1. 提交直邮表面。

您现在可以 [创建直邮消息](../direct-mail/create-direct-mail.md) 在营销活动中。 营销活动开始后，包含目标受众数据的文件将自动导出到您定义的服务器。 然后，直邮提供商将能够检索该文件并继续直邮投放。

>[!NOTE]
>
>自动从文件中删除行中所有值都相同的重复行。

<!--
    In the **[!UICONTROL Insertion]** section, you can choose to automatically remove duplicate rows.

    Define the maximum number of records (i.e. rows) for each file containing profile data. After the specified threshold is reached, another file will be created for the remaining records.

    ![](assets/surface-direct-mail-split.png)

    For example, if there are 100,000 records in the file and the threshold limit is set to 60,000, the records will be split into two files. The first file will contain 60,000 rows, and the second file will contain the remaining 40,000 rows.

    >[!NOTE]
    >
    >NOTE You can set any number between 1 and 200,000 records, meaning each file must contain at least 1 row and no more than 200,000 rows.

-->