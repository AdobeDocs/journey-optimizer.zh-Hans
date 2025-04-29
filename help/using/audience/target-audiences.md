---
solution: Journey Optimizer
product: journey optimizer
title: 关于 Adobe Experience Platform 受众
description: 了解如何使用 Adobe Experience Platform 受众
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 78b95ccd-bc28-46cd-937a-f68e3f34cc1e
source-git-commit: 0f3191a3d7c5c78e1d8fac2e587e26522f02f8f5
workflow-type: tm+mt
source-wordcount: '660'
ht-degree: 22%

---

# [!DNL Journey Optimizer]中的受众激活 {#segments-in-journey-optimizer}

您可以在营销活动和历程中选择使用区段定义、自定义上传、组合工作流或联合受众组合生成的任何受众。

>[!AVAILABILITY]
>
>受众构成中的受众和属性当前不能用于Healthcare Shield或Privacy and Security Shield。 [了解如何在Journey Optimizer中使用受众扩充属性](../audience/about-audiences.md#enrichment)

## 受众激活延迟 {#activation}

受众可在摄取完成后立即在Journey Optimizer中使用。 虽然该值通常在一小时内，但受制于一些可变因素。 合成产生的受众应在发布后24小时内可用。

对于批量分段作业产生的受众，激活可能会由于批量摄取可变性而延迟。 对于安排在每天的读取受众历程，您可以在历程属性中定义一个时间窗口，以确保在历程执行之前有新的受众数据可用。 如果分段作业未在定义的时间范围内完成，则将跳过历程，直到下一次出现该历程。 [了解如何计划读取受众历程](../building-journeys/read-audience.md)

>[!AVAILABILITY]
>
>**[!UICONTROL 批量受众评估后触发]**&#x200B;选项仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。

## 自定义上传和联合受众构成

对于自定义上传和联合受众合成受众，请注意以下护栏：

* **预览和验证支持：**&#x200B;当前，使用CSV上传或联合受众组合创建的受众不支持预览和验证。 在规划营销活动时，请牢记这一点。

* **定向新配置文件：**&#x200B;当记录与UPS配置文件之间找不到匹配项时，将创建一个新的空配置文件。 此配置文件链接到存储在数据湖中的扩充属性。 由于此新配置文件为空，因此Journey Optimizer中通常使用的定向字段（例如personalEmail.address、mobilePhone.number）为空，因此无法用于定向。

  要解决此问题，您可以在渠道配置中将“执行字段”（或“执行地址”，具体取决于渠道）指定为“identityMap”。 这将确保在创建受众时选择作为标识的属性将与Journey Optimizer中用于定位的属性相同。

* **已激活的记录和身份拼接：**&#x200B;已激活受众中的每个记录，包括任何重复项。 在下次UPS配置文件导出期间，这些记录将进行身份拼接。 因此，激活的记录数可能与身份拼接后的用户档案数不同。

## 在[!DNL Journey Optimizer]中定位受众

您可通过不同方式在 **[!DNL Journey Optimizer]** 中利用受众：

* 为&#x200B;**营销活动**&#x200B;选择受众，消息将发送给属于所选受众的所有个人。[了解如何定义营销活动的受众](../campaigns/create-campaign.md#define-the-audience-audience)。

* 在历程中使用&#x200B;**读取受众**&#x200B;编排活动，使受众中的所有个人进入历程并接收历程中包含的消息。 假设您拥有“白银客户”受众。通过此活动，您可以使所有白银客户进入历程，并向其发送一系列个性化消息。[了解如何配置读取受众活动](../building-journeys/read-audience.md#configuring-segment-trigger-activity)。

  >[!NOTE]
  >
  >任何在“读取受众”活动中使用受众构成或自定义上传的受众的历程都将具有与上次批次评估一样全新的配置文件属性。 这包括历程中的同意/抑制。

* 使用历程中的&#x200B;**条件**&#x200B;活动，根据受众成员资格构建条件。[了解如何在条件中使用受众](../building-journeys/condition-activity.md#using-a-segment)。

* 在历程中使用&#x200B;**受众资格**&#x200B;事件活动，根据Adobe Experience Platform受众进入和退出，让个人进入历程或在此历程中前进。 例如，您可以让所有新的白银客户进入历程并向其发送消息。有关如何使用此活动的更多信息，请参阅[了解如何配置受众资格筛选活动](../building-journeys/audience-qualification-events.md)。

  >[!NOTE]
  >
  >由于使用组合工作流、自定义上传或联合受众组合创建的受众的批量性质，无法在“受众资格”活动中定位这些受众。 此活动中只能利用使用区段定义创建的受众。
