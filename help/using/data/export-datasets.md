---
solution: Journey Optimizer
product: journey optimizer
title: 将数据集导出到云存储位置
description: 了解如何使用Adobe Experience Platform云存储目标导出数据集。
role: User
level: Beginner
badge: label="Beta" type="Informitive"
keywords: 平台，数据湖，创建，湖，数据集，配置文件
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: c823d1a02ca9d24fc13eaeaba2b688249e61f767
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 4%

---

# 将数据集导出到云存储位置 {#export-datasets}

>[!AVAILABILITY]
>
>数据集导出功能目前为测试版，可供所有Adobe Journey Optimizer用户使用。 如果您尚未拥有访问权限，请与 Adobe 代表联系，获取目标的访问权限。

Journey Optimizer允许您与云存储位置建立实时连接，以导出数据集的内容。

通过定期导出数据，您可以确保客户交互有完整且最新的记录，将此信息用于报告或分析，并保持符合法律要求。

## 可用的云存储目标 {#destinations}

您可以将数据集导出到6个云存储目标，这些目标可从 **[!UICONTROL 目标]** 菜单中 **[!UICONTROL 目录]** 选项卡。

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>这些目标均在测试版中提供，并且可能会发生更改。

有关每个目标的详细信息，请参阅Adobe Experience Platform文档：

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html)
* [Azure数据湖第2代](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html)
* [数据登陆区](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html)
* [Google云存储](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html)

## 先决条件 {#prerequisites}

开始导出数据集之前，请检查以下先决条件：

* 要导出数据集，您需要 **管理目标**, **查看目标**, **激活目标**&#x200B;和 **管理和激活数据集目标** [访问控制权限](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html#permissions). 阅读 [访问控制概述](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html) 或联系您的产品管理员以获取所需的权限。

* 此功能仅支持导出第一代数据，即在 [Real-time Customer Data Platform产品说明](https://helpx.adobe.com/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). 确保要导出的数据集不包含第二代数据。

## 导出数据集的主要步骤 {#main-steps}

将数据集导出到云存储位置的主要步骤如下：

![](assets/dataset-export-process.png)

有关每个步骤的详细信息，请参阅Adobe Experience Platform文档： [将数据集导出到云存储目标](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=en).

1. **设置云存储目标**. 如果您尚未执行此操作，请从目标目录连接到云存储目标。 [了解如何创建新目标连接](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=en#setup)

   <!--![](assets/dataset-export-setup.png)-->

1. **选择云存储目标** 以导出数据集。 在目标目录中，单击 **[!UICONTROL 导出数据集]** 按钮，然后选择要使用的连接。

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >如果您将Adobe Journey Optimizer与实时客户配置文件一起使用，则目标卡将显示“激活”按钮，允许您根据您启用的权限导出数据集并激活此目标的区段。

1. **选择数据集** 要导出到选定目标的URL。

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **计划导出** 的次数。 指定导出应何时开始以及应以哪个频率进行。

   <!--![](assets/dataset-export-schedule.png)-->

1. **查看并确认导出** 通过检查在配置结束时显示的摘要。

   <!--![](assets/dataset-export-review.png)-->

导出完成后，数据集的内容会根据您配置的计划存储到云存储位置。 [了解如何验证数据集导出是否成功](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html#verify)
