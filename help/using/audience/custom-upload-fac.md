---
solution: Journey Optimizer
product: journey optimizer
title: 自定义上传(CSV)和联合受众合成
description: 了解使用自定义上传(CSV)和联合受众组合受众时的关键信息和最佳实践。
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
source-git-commit: 26d311802236a1f9e8f6273c1291bcb54138aad2
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 6%

---

# 自定义上传(CSV)和联合受众合成 {#csv-fac}

## 关于自定义上传和联合受众构成 {#about}

除了区段定义和受众构成之外，[!DNL Journey Optimizer]还允许您通过从CSV文件导入受众或利用数据仓库中的数据来生成和定位受众。

* **自定义上传**：使用CSV文件导入受众。 请参阅Adobe Experience Platform [Segmentation Service文档](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-portal#import-audience){target="_blank"}以了解如何导入受众。

* **联合受众构成**：直接从现有数据仓库联合数据集，以在一个系统中构建和扩充Adobe Experience Platform受众和属性。 请阅读有关[联合受众组合](https://experienceleague.adobe.com/zh-hans/docs/federated-audience-composition/using/home)的指南。

  >[!AVAILABILITY]
  >
  >联合受众构成目前仅对一部分组织提供（限量发布）。有关更多信息，请与您的 Adobe 代表联系。

您可以在Journey Optimizer中定位这些受众，或将其激活到Adobe Experience Platform支持的任何目标

➡️[在视频中发现这些功能](#video)

## 必读 {#must-read}

本节提供了在使用自定义上传（CSV文件）和联合受众合成受众时要记住的关键信息。

* **预览和验证支持：**&#x200B;当前，使用CSV上传或联合受众组合创建的受众不支持预览和验证。 在规划营销活动时，请牢记这一点。

* **激活延迟：**&#x200B;受众可在摄取完成后立即在Journey Optimizer中使用。 虽然该值通常在一小时内，但受制于一些可变因素。

* **已激活的记录和身份拼接：**&#x200B;已激活受众中的每个记录，包括任何重复项。 在下次UPS配置文件导出期间，这些记录将进行身份拼接。 因此，激活的记录数可能与身份拼接后的用户档案数不同。

* **定向新配置文件：**&#x200B;当记录与UPS配置文件之间找不到匹配项时，将创建一个新的空配置文件。 此配置文件链接到存储在数据湖中的扩充属性。 由于此新配置文件为空，因此Journey Optimizer中通常使用的定向字段（例如personalEmail.address、mobilePhone.number）为空，因此无法用于定向。

  要解决此问题，您可以在渠道配置中将“执行字段”（或“执行地址”，具体取决于渠道）指定为“identityMap”。 这将确保在创建受众时选择作为标识的属性将与Journey Optimizer中用于定位的属性相同。

## 操作说明视频 {#video}

了解如何将CSV格式的受众上传到Adobe Experience Platform。

>[!VIDEO](https://video.tv.adobe.com/v/3421714?quality=12)

了解有关联合受众构成的更多信息。

>[!VIDEO](https://video.tv.adobe.com/v/3432261?quality=12)
