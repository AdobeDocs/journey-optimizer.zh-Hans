---
solution: Journey Optimizer
product: journey optimizer
title: 重试
description: 了解在将地址发送到禁止列表之前如何执行重试
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 重试，退回，软退回，优化器，错误
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 13%

---

# 重试 {#retries}

当电子邮件由于临时原因失败时 **软退回** 错误，将执行多次重试。 每个错误都会递增一个错误计数器。 当此计数器达到限制阈值时，地址将添加到禁止列表。

>[!NOTE]
>
>了解更多有关错误类型的信息，请参见 [投放失败类型](../reports/suppression-list.md#delivery-failures) 部分。

在默认配置中，阈值设置为5错误。

* 对于同一投放，在第五次遇到以下错误： [重试时段](#retry-duration)，则地址会被隐藏。

* 如果存在不同的投放，并且至少相隔24小时发生两个错误，则错误计数器在每次错误时递增，并且在第五次尝试时也抑制地址。

如果重试后投放成功，则地址的错误计数器将重新初始化。

## 重试阈值版本 {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="更新重试阈值"
>abstract="如果默认值不适合需求，您可以修改允许的连续软退回次数。对于特定电子邮件地址，当重试计数器达到错误阈值时，此地址将添加到禁止列表中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html?lang=zh-Hans" text="了解禁止列表"

如果默认值5不符合您的需要，您可以按照以下步骤修改错误阈值。

1. 转到 **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件配置]** > **[!UICONTROL 禁止显示列表]**.

1. 选择 **[!UICONTROL 编辑禁止显示规则]** 按钮。

   ![](assets/suppression-list-edit-retries.png)

1. 根据需要编辑允许的连续软退回次数。

   ![](assets/suppression-list-edit-soft-bounces.png)

   必须输入一个介于1和20之间的整数值，这意味着最小重试次数是1，最大重试次数是20。

   >[!CAUTION]
   >
   >列入阻止列表任何大于10的值都可能导致可投放性信誉问题，以及ISP的IP节流或。 [了解关于可投放性的更多信息](../reports/deliverability.md)

## 重试时段 {#retry-duration}

此 **重试时段** 是重试遇到临时错误或软退回的投放的任何电子邮件消息的时间范围。

默认情况下，将对以下对象执行重试 **3.5天** (或 **84小时**)时，发送电子邮件给管理员。

但是，为了确保不再需要时不会执行重试尝试，您可以在创建或编辑时根据需要更改此设置 [渠道表面](channel-surfaces.md) （即消息预设）应用于电子邮件渠道。

例如，对于与密码重置相关并包含仅在一天内有效的链接的事务性电子邮件，您可以将重试期限设置为24小时。 同样，对于午夜促销，您可能希望定义6小时的重试时段。

>[!NOTE]
>
>重试时间不能超过84小时。 营销电子邮件的最小重试期限为6小时，事务电子邮件的最小重试期限为10分钟。

了解在中创建渠道表面时如何调整电子邮件重试参数 [本节](../email/email-settings.md#email-retry).

