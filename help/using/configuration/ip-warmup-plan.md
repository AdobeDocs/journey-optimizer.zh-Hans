---
solution: Journey Optimizer
product: journey optimizer
title: 创建IP预热计划
description: 了解如何在Journey Optimizer中创建IP预热计划
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP、组、子域、可投放性
hide: true
hidefromtoc: true
exl-id: c2434086-2ed4-4cd0-aecd-2eea8f0a55f6
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 14%

---

# 创建IP预热计划 {#ip-warmup}

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [IP预热入门](ip-warmup-gs.md)
* [创建 IP 预热营销活动](ip-warmup-campaign.md)
* **[创建IP预热计划](ip-warmup-plan.md)**
* [执行IP预热计划](ip-warmup-execution.md)

>[!ENDSHADEBOX]

创建了一个或多个 [IP预热活动](ip-warmup-campaign.md) 启用专用接口和相应的选项后，即可开始创建IP预热计划。

## 准备IP预热计划文件 {#prepare-file}

IP预热是一项活动，包括逐渐增加从您的IP和域发送到主要Internet服务提供商(ISP)的电子邮件数量，以确立您作为合法发件人的声誉。

此活动通常在可投放性专家的帮助下执行，该专家有助于根据行业域、用例、地区、ISP和各种其他因素制定周全的计划。

使用时 [!DNL Journey Optimizer] IP预热功能，此计划采用Excel文件的形式，该文件必须包含大量预定义列。 在中创建IP预热计划之前 [!DNL Journey Optimizer] 界面，您需要使用此模板填写将提供计划的所有数据。

>[!CAUTION]
>
>请与您的可投放性顾问合作，确保您的IP预热计划文件设置正确。

以下是包含IP预热计划的文件示例。

![](assets/ip-warmup-sample-file.png)

### “IP预热计划”选项卡

* 在此示例中，已准备了跨越17天的计划(称为“**运行**“)以实现超过100万用户档案的目标数量。

* 此计划的执行截止日期为6 **阶段**，每个报表包至少包含一个运行。

* 对于要交付到的域，您可以拥有任意数量的列。 在此示例中，计划分为6列：其中5列对应于 **主域组** 用于您的计划(Gmail、Microsoft、Yahoo、Orange和Apple)和第六列， **其他**，包含其他域的所有剩余地址。
* 此 **参与天数** 列显示仅定向过去30天内与您的品牌互动的用户档案。

其思想是逐步增加每次运行的目标地址数量，同时减少每个阶段的运行数量。

下面列出了可添加到计划中的现成主域组：

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

您还可以通过包含自定义域组向计划添加更多列。

使用 **[!UICONTROL 自定义域组]** 选项卡来定义新域组。 对于每个域，您可以添加它涵盖的所有子域。<!--TBC-->

例如，如果添加自定义域Luma，则需要包含以下子域：luma.com、luma.co.uk、luma.it、luma.fr、luma.de等。

## 访问和管理IP预热计划 {#manage-ip-warmup-plans}

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单。 此时将显示迄今为止创建的所有IP预热计划。

   ![](assets/ip-warmup-filter-list.png)

1. 您可以对状态进行过滤。 不同的状态包括：

   * **未开始**：尚未激活任何运行。 [了解详情](ip-warmup-execution.md#define-runs)
   * **实时**：一旦成功激活第一阶段的第一次运行，计划就会更改为此状态。 [了解详情](ip-warmup-execution.md#define-runs)
   * **已完成**：计划已标记为已完成。 仅当计划中的所有运行都位于以下位置时，此选项才可用 **[!UICONTROL 已成功]** 或 **[!UICONTROL 草稿]** 状态(无法运行 **[!UICONTROL 实时]**)。 [了解详情](ip-warmup-execution.md#define-runs#mark-as-completed)
     <!--* **Paused**: to check (user action)-->

1. 要删除IP预热计划，请选择 **[!UICONTROL 删除]** 图标并确认删除。

   ![](assets/ip-warmup-delete-plan.png)

   >[!CAUTION]
   >
   >选定的IP预热计划将被永久删除。

## 创建IP预热计划 {#create-ip-warmup-plan}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_upload"
>title="指定 IP 预热计划"
>abstract="下载 CSV 模板并在其中填入 IP 预热阶段的数据和配置文件的目标数量。"

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_surface"
>title="选择营销表面"
>abstract="您必须选择在要与您的 IP 预热计划关联的营销活动中选择的相同表面。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="设置渠道表面"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/channel-surfaces.html" text="创建 IP 预热营销活动"

当一个或多个实时营销活动具有 **[!UICONTROL IP预热计划激活]** 启用选项后，您可以将其与IP预热计划关联。

>[!CAUTION]
>
>要创建、编辑和删除IP预热计划，您必须具有 **[!UICONTROL 可投放性顾问]** 许可。 <!--Learn more on managing [!DNL Journey Optimizer] users' access rights in [this section](../administration/permissions-overview.md).-->

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL IP预热计划]** 菜单，然后单击 **[!UICONTROL 创建IP预热计划]**.

   ![](assets/ip-warmup-create-plan.png)

1. 填写IP预热计划详细信息：提供名称和描述。

   ![](assets/ip-warmup-plan-details.png)

1. 选择 [曲面](channel-surfaces.md). 仅营销表面可供选择。 [了解有关电子邮件类型的更多信息](../email/email-settings.md#email-type)

   >[!CAUTION]
   >
   >您必须选择在要与您的 IP 预热计划关联的营销活动中选择的相同表面。[了解如何创建IP预热活动](ip-warmup-campaign.md)

1. 上载包含IP预热计划的Excel文件。 [了解详情](#prepare-file)

   <!--
    You can also download the Excel template from the [!DNL Journey Optimizer] user interface and upload it after filling it with the IP warmup details.-->

   ![](assets/ip-warmup-upload-success.png)

1. 单击&#x200B;**[!UICONTROL 创建]**。在上传的文件中定义的所有阶段、运行、列及其内容会自动显示在 [!DNL Journey Optimizer] 界面。 [了解详情](ip-warmup-execution.md)

   ![](assets/ip-warmup-plan-uploaded.png)
