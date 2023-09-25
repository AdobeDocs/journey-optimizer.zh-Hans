---
solution: Journey Optimizer
product: journey optimizer
title: 创建IP预热计划
description: 了解如何创建IP预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、池、组、子域、可投放性
hide: true
hidefromtoc: true
source-git-commit: 1ec2c406e777e08de97c3ad53cee5986afeb3c44
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 5%

---

# 创建IP预热计划 {#ip-warmup}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [IP预热入门](ip-warmup-gs.md)
* [创建IP预热活动](ip-warmup-campaign.md)
* **[创建IP预热计划](ip-warmup-plan.md)**
* [运行IP预热计划](ip-warmup-running.md)

>[!ENDSHADEBOX]

创建了一个或多个 [IP预热活动](ip-warmup-campaign.md) 启用专用接口和相应的选项后，即可开始创建IP预热计划。

## 填写IP预热模板 {#upload-plan}

在Journey Optimizer界面中创建IP预热计划之前，您需要使用Excel格式填写模板，其中包含将提供计划的所有数据。

>[!CAUTION]
>
>请与您的可投放性顾问合作，确保您的IP预热计划文件设置正确。

以下是包含IP预热计划的文件示例。

![](assets/ip-warmup-sample-file.png)

### “IP预热计划”选项卡

IP预热是一项活动，包括逐渐增加从您的IP和域发送到主要Internet服务提供商(ISP)的电子邮件数量，以确立您作为合法发件人的声誉。

此活动通常在可交付性顾问或专家的帮助下执行，该顾问或专家根据行业领域、用例、地区、ISP和各种其他因素制定经过深思熟虑的计划。

* 在此示例中，已准备了一个跨越17天的计划，以达到xxx个配置文件的目标数量。

* 该计划分六个阶段执行。

* 对于要交付到的域，您可以拥有任意数量的列。 在本例中，计划被分为四列，对应于要在计划中使用的域组：Gmail、Adobe、Yahoo等。

其思想是在第一阶段运行更多地址，并逐步增加目标地址的数量，同时减少运行次数。

现成域的列表如下：

* Gmail
* Adobe
* WP
* Comcast
* Yahoo
* 大池塘
* 橙色
* 软银
* 杜科莫
* 联合互联网
* Microsoft
* KDDI
* 意大利在线
* 拉波斯特
* Apple

### “自定义域组”选项卡

您还可以为自定义域组添加更多列。

使用 **[!UICONTROL 自定义域组]** 选项卡，以定义新域，并为每个域添加它包含的所有子域。<!--TBC-->

## 访问和管理IP预热计划 {#manage-ip-warmup-plans}

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单。 此时将显示迄今为止创建的所有IP预热计划。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以对状态进行过滤。 不同的状态包括：

   * **未开始**：尚未激活任何运行。 [了解详情](ip-warmup-running.md#define-runs)
   * **进行中/实时**：一旦成功激活第一阶段中的第一次运行，计划即采取此状态。 [了解详情](ip-warmup-running.md#define-runs)
   * **已完成**：计划已标记为已完成。 仅当计划中的所有运行都位于以下位置时，此选项才可用 **[!UICONTROL 已成功]** 或 **[!UICONTROL 草稿]** 状态(无法运行 **[!UICONTROL 实时]**)。 [了解详情](ip-warmup-running.md#define-runs#mark-as-completed)
   * **已暂停**<!--: to check (user action)-->

1. 要删除IP预热计划，请选择 **[!UICONTROL 删除]** 图标并确认删除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >选定的IP预热计划将被永久删除。

## 创建IP预热计划 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定IP预热计划"
>abstract="下载CSV模板，并使用IP预热阶段的数据和目标配置文件数填充该模板。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="选择营销表面"
>abstract="必须选择与要在营销策划中与IP预热计划关联的所选表面相同的表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="设置渠道表面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="创建IP预热活动"

当一个或多个实时营销活动具有 **[!UICONTROL IP预热计划激活]** 启用选项后，您可以将其与IP预热计划关联。

>[!CAUTION]
>
>要创建、编辑和删除IP预热计划，您必须具有 **[!UICONTROL 可投放性顾问]** 许可。 <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->
>
>与您的可投放性顾问合作，确保您的IP预热计划模板设置正确。 <!--TBC-->

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单，然后单击 **[!UICONTROL 创建IP预热计划]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填写IP预热计划详细信息：提供名称和描述。

   ![](assets/ip-warmup-plan-details.png)

1. 选择 [曲面](channel-surfaces.md). 仅营销表面可供选择。 [了解有关电子邮件类型的更多信息](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >必须选择与要在营销策划中与IP预热计划关联的所选表面相同的表面。 [了解如何创建IP预热活动](#create-ip-warmup-campaign)

1. 上载包含IP预热计划的Excel文件<!--which formats are allowed?-->. 您可以使用可交付性团队提供的模板。<!--TBC?--> [了解详情](#upload-plan)
   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。上传的文件中定义的阶段数将自动显示，每个阶段的所有运行都将自动显示。 [了解详情](#upload-plan)

   ![](assets/ip-warmup-plan-phases.png)

## 重新上传IP预热计划 {#re-upload-plan}

您可以使用相应的按钮重新上传另一个IP预热计划。

![](assets/ip-warmup-re-upload-plan.png)

>[!NOTE]
>
>IP预热计划的详细信息将根据新上传的文件而更改。 完整运行和激活的运行不受影响。