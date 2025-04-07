---
solution: Journey Optimizer
product: journey optimizer
title: 重试
description: 了解在将地址发送到禁止列表之前如何执行重试
feature: Deliverability, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: 重试，退回，软退回，优化器，错误
exl-id: 05564a99-da50-4837-8dfb-bb1d3e0f1097
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '578'
ht-degree: 9%

---

# 重试 {#retries}

当电子邮件因给定地址的临时&#x200B;**软退回**&#x200B;错误而失败时，将执行多次重试。 每个错误都会递增一个错误计数器。 当此计数器达到限制阈值时，电子邮件地址将添加到禁止列表。

>[!NOTE]
>
>详细了解[投放失败类型](../reports/suppression-list.md#delivery-failures)部分中的错误类型。

在默认配置中，阈值设置为5错误。

* 对于同一投放，在[重试时段](#retry-duration)内遇到第5个错误，将禁止显示该地址。

* 如果存在不同的投放，并且至少间隔24小时发生两个错误，则错误计数器在每次错误时递增，并且在第五次尝试时也抑制地址。 每个地址的错误是累积的。

如果重试后投放成功，则地址的错误计数器将重新初始化。

例如：

* 您在星期一发送一封电子邮件，其重试时间段设置为24小时。 emma.jones@mail.com地址无法送达。 电子邮件最多重试三次，并在达到24小时的重试时段时停止重试。

* 您周三又发送了一封电子邮件。 已经存在三个错误数的emma.jones@mail.com也已被定向，并且再次无法投放 — 两次。 此外还有两个错误。

如果未尝试其他投放，并且在这两封电子邮件之间成功投放，则会将emma.jones@mail.com地址添加到禁止列表，因为3 + 2个错误的累积影响。

## 重试编辑阈值 {#edit-retry-threshold}

>[!CONTEXTUALHELP]
>id="ajo_admin_suppression_list_bounces"
>title="更新重试阈值"
>abstract="如果默认值不适合需求，您可以修改允许的连续软退回次数。对于特定电子邮件地址，当重试计数器达到错误阈值时，此地址将添加到禁止列表中。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/reporting/deliverability/suppression-list.html" text="了解禁止列表"

如果默认值5不符合您的需要，您可以按照以下步骤修改错误阈值。

1. 转到&#x200B;**[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 禁止显示列表]**。

1. 选择&#x200B;**[!UICONTROL 编辑禁止显示规则]**&#x200B;按钮。

   ![](assets/suppression-list-edit-retries.png)

1. 根据需要编辑允许的连续软退回次数。

   ![](assets/suppression-list-edit-soft-bounces.png)

   必须输入介于1和20之间的整数值，这意味着最小重试次数是1，最大重试次数是20。

   >[!CAUTION]
   >
   >任何大于10的值都可能导致可投放性信誉问题，以及ISP的IP限制或列入阻止列表。 [了解有关可投放性的更多信息](../reports/deliverability.md)

## 重试时段 {#retry-duration}

**重试时段**&#x200B;是任何遇到临时错误或软退回的投放电子邮件将重试的时间范围。

默认情况下，从将邮件添加到电子邮件队列起，将执行重试&#x200B;**3.5天**（或&#x200B;**84小时**）。

但是，为了确保不再需要时重试尝试，您可以在创建或编辑应用于电子邮件渠道的[渠道配置](channel-surfaces.md)（即消息预设）时根据需要更改此设置。

例如，对于与密码重置相关的事务性电子邮件，如果其中包含仅在一天内有效的链接，您可以将重试期限设置为24小时。 同样，对于午夜促销，您可能希望定义6小时的重试时段。

>[!NOTE]
>
>重试时间不能超过84小时。 营销电子邮件的最小重试期限为6小时，事务电子邮件的最小重试期限为10分钟。

了解在[本节](../email/email-settings.md#email-retry)中创建渠道配置时如何调整电子邮件重试参数。

