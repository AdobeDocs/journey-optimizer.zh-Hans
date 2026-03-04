---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件渠道配置中的CC（抄送）
description: 在Journey Optimizer电子邮件渠道中配置可见的抄送收件人。 了解如何设置CC字段、它与BCC的区别以及限制。
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
hide: true
hidefromtoc: true
keywords: 抄送、抄送、电子邮件、渠道配置、电子邮件标头、密件抄送
badge: label="限量发布版" type="Informative"
exl-id: 9649cc07-3183-4510-b5d9-b1e33eff43e9
source-git-commit: 780a9259ee081336d1efb3e38c2a8eee4e97b7e3
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 1%

---

# 向电子邮件添加抄送字段 {#cc-email-field}

>[!CONTEXTUALHELP]
>id="ajo_admin_config_cc"
>title="定义“抄送”电子邮件地址"
>abstract="您可以向使用此渠道配置发送的电子邮件添加可见CC（抄送）字段。 输入固定电子邮件地址或使用个性化（用户档案属性或上下文变量）。 请注意，CC使用量计入您的授权消息量。"

>[!AVAILABILITY]
>
>此功能仅对有限可用的所有客户可用。 请联系 Adobe 代表获取访问权限。

您可以向[!DNL Journey Optimizer]通过您的历程和营销活动发送的电子邮件添加可见CC（抄送）字段。 此可选功能在[渠道配置](channel-surfaces.md)级别配置，以及电子邮件标头参数和密件抄送电子邮件选项。

>[!CAUTION]
>
>CC功能使用量根据您获得许可的邮件数计算。 仅在需要显示CC收件人的位置启用它。 检查您的合同中是否有许可卷。

与[密件抄送](archiving-support.md#bcc-email)一样，“抄送”字段用于将电子邮件的副本发送到其他地址。 但是，它与BCC在以下方面有所不同：

* 抄送电子邮件地址对主要收件人可见，因此它使主要收件人能够查看被复制的人并了解联系谁进行跟进。
* 与密件抄送不同，抄送电子邮件字段支持个性化，这使您能够为许多方案使用一个渠道配置，并将副本发送给每个收件人的正确人员（例如，其关系经理）。 对于API触发的营销活动，这允许您cc与特定事件或交易相关的地址。

>[!NOTE]
>
>如果需要保留地址不可对收件人可见的副本，以进行存档或遵循操作，请使用[密件抄送](archiving-support.md#bcc-email)，而不要使用“抄送”。

## 启用“抄送电子邮件” {#enable-cc}

要启用&#x200B;**[!UICONTROL 抄送电子邮件]**&#x200B;选项，请在[电子邮件渠道配置](../email/email-settings.md)中配置“抄送”字段。

![](assets/email-config-cc.png)

除了在委派给Adobe的子域上定义的电子邮件地址之外，您可以按正确格式指定任何外部地址。 例如，如果您已将&#x200B;*marketing.luma.com*&#x200B;子域委派给Adobe，则禁止使用&#x200B;*abc@marketing.luma.com*&#x200B;等任何地址。

>[!CAUTION]
>
>您只能定义一个电子邮件地址。 确保抄送地址有足够的接收容量来存储使用当前渠道配置发送的所有电子邮件。
>
>[此部分](#cc-recommendations-limitations)中列出了更多推荐。

**[!UICONTROL 抄送电子邮件]**&#x200B;字段接受三种类型的值：

* 一个&#x200B;**硬编码值**，该值可以是固定的电子邮件地址。

* **配置文件属性**，如配置文件中可用的关系管理器电子邮件地址。

* **上下文属性** — 此值&#x200B;**只能用于API触发的营销活动**。 它从API有效负载中检索，该API有效负载必须包含具有CC地址值的上下文变量`context.channel.email.ccvalues`。

  >[!WARNING]
  >
  >使用&#x200B;**上下文变量**&#x200B;设置CC时，只有&#x200B;**API触发的营销活动**&#x200B;才支持它。 如果您在历程或操作营销活动中使用该渠道配置，则电子邮件仅发送给主要收件人；不会向CC地址发送副本。

邮件中包含的任何[附件](../email/pdf-attachments.md)都会同时发送到主要收件人和抄送地址。

如果抄送值在发送时无效或缺失（例如，空的上下文变量），则会跳过抄送副本；主收件人仍会收到电子邮件。

如果“抄送”字段有多个值（例如，使用配置文件属性或解析为多个地址的表达式时），则仅使用第一个值发送电子邮件。

## 在现有渠道配置中编辑抄送电子邮件 {#cc-edit}

如果您[编辑电子邮件配置](channel-surfaces.md#edit-channel-surface)并添加或更改“抄送”字段，则只能使用：

* **硬编码**&#x200B;抄送电子邮件地址，或
* **上下文变量**（用于API触发的使用）。

>[!CAUTION]
>
>编辑现有电子邮件渠道配置时，无法向[抄送电子邮件](../personalization/personalization-build-expressions.md#sources)字段添加新的&#x200B;**[!UICONTROL 配置文件属性]**。 您必须创建[新渠道配置](channel-surfaces.md#create-channel-surface)。

## 建议和限制 {#cc-recommendations-limitations}

* **权利：**&#x200B;抄送使用情况已计入您的授权邮件卷。 仅在需要可见抄送收件人的情况下使用抄送。 检查您的合同中是否有许可卷。

* **隐私和合规性：**&#x200B;为确保您的隐私合规性，抄送电子邮件必须由能够安全存储个人身份信息(PII)的系统进行处理（如果适用）。 由于邮件可能包含敏感或私有数据（如PII），因此请确保CC地址正确并且保护对邮件的访问。

* **收件箱管理：**&#x200B;您用于CC的收件箱应正确管理空间和投放。 如果收件箱返回退件，则可能无法接收某些电子邮件。

* **传递时间：**&#x200B;邮件可在目标收件人之前传递到“抄送”电子邮件地址。 即使原始邮件可能有[退回](../reports/suppression-list.md#delivery-failures)，也可以发送CC邮件。

* **报告：**&#x200B;来自抄送收件人的打开次数、点击次数和其他参与情况包含在电子邮件报告量度中。 因此，抄送收件人的任何打开或点击都将导致[报告](../reports/report-gs-cja.md)计算错误。

* **垃圾邮件：**&#x200B;请勿在“抄送”收件箱中将邮件标记为垃圾邮件，因为它将影响发送到此地址的所有其他电子邮件。

* **可投放性：**&#x200B;使用符合发送实践和收件人期望的抄送。 过度使用CC可能会影响可投放性；请遵循[可投放性最佳实践](../reports/deliverability.md)和您的合同条款。

>[!CAUTION]
>
>请勿单击发送到抄送地址的电子邮件中的取消订阅链接，因为您将立即取消订阅&#x200B;**To**&#x200B;电子邮件收件人。
