---
solution: Journey Optimizer
product: journey optimizer
title: CNIL关于电子邮件跟踪像素的指南
description: 了解CNIL关于电子邮件跟踪像素的更新指南，以及可支持您的合规工作的Adobe Journey Optimizer控件。
feature: Privacy, Consent Management
topic: Content Management
role: User
level: Intermediate
keywords: CNIL，跟踪，像素，电子邮件，同意，选择退出，隐私
source-git-commit: 24d6a17d57ede317d3f04add2fd01bd3ff0ab9af
workflow-type: tm+mt
source-wordcount: '1490'
ht-degree: 2%

---


# 了解CNIL关于电子邮件跟踪像素的更新指南 {#cnil-pixel-tracking}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解CNIL于2026年4月提出的关于电子邮件跟踪像素的建议并发现Adobe Journey Optimizer控件（打开跟踪切换、链接级别跟踪、同意管理、选择退出机制和禁止）可支持您的合规工作。

>[!ENDSHADEBOX]

>[!NOTE]
>
>此页面仅供参考。 这不是法律建议，也不保证您遵守适用法律。 下面描述的Adobe Journey Optimizer产品功能是构建块，经过适当配置和操作后，可以支持合规的实施。 每位客户均须负责决定及履行其于适用法律下之责任。

## 概述 {#overview}

2026年4月14日，法国数据保护机构&#x200B;*全国信息和自由委员会* (CNIL)发布了关于在电子邮件中使用跟踪像素的[建议](https://www.cnil.fr/sites/default/files/2026-04/recommandation-pixels_de_suivi.pdf)。 该指南阐明何时需要获得同意，并强调针对电子邮件像素跟踪的适当同意实践的重要性。 此策略可能会影响向位于法国的订阅者发送电子邮件的任何实体的发送实践。

CNIL提供了自建议之日起三个月的时间，要求公司通知其电子邮件收件人（“用户”）跟踪像素的存在、其目的以及用户选择退出的权利。 在此过渡期间，客户应通知用户像素跟踪信息，并在必要时提供选择退出选项。 预计CNIL将在2026年7月14日之后开始执行活动。

随着CNIL和其他监管机构澄清有关跟踪像素和相关问题的指导，Adobe将继续监控更新，并告知客户支持电子邮件营销的Adobe产品（包括Adobe Journey Optimizer）的技术功能。

Adobe Journey Optimizer提供的控制可帮助客户在交付级别管理打开跟踪。 根据适用的CNIL指导和其他法律，客户有责任确定自己的合规义务，但这些功能可能会为客户合规工作提供支持。

## 什么是电子邮件跟踪像素 {#tracking-pixel}

电子邮件跟踪像素是嵌入到电子邮件HTML中的1x1透明图像。 收件人的电子邮件客户端加载该图像时，像素会向服务器发出ping信号，该信号记录时间戳、设备类型、电子邮件客户端等数据，有时还会记录IP地址以大致了解位置。 然后，该日志将绑定到收件人的记录，以允许营销人员查看电子邮件是否已打开。

## 客户支持 {#support}

为实施上述更改寻求帮助的客户可以与其现有的Adobe生态系统合作。 有关所引用Adobe功能的技术问题，请联系您的客户成功经理或技术客户经理。

## 与电子邮件跟踪相关的Adobe Journey Optimizer功能 {#ajo-functionality}

Adobe Journey Optimizer提供了几个本机控件，以帮助客户处理CNIL指南中的元素。 以下各部分介绍了相关的产品功能。

### 电子邮件类型分类 {#email-type}

在Adobe Journey Optimizer中，每个电子邮件渠道配置都分类为“营销”或“事务性”。 此分类确定在发送之前是否需要订阅者同意。

* **营销电子邮件**：向选择加入的订阅者发送促销通信。 需要用户同意。 这些电子邮件会自动遵循禁止显示和选择退出偏好设置。
* **事务性电子邮件**：非商业通信（例如，订单确认、密码重置）。 根据适用的法律，这些消息可以发送给已取消订阅营销通信的用户档案。

电子邮件类型在渠道配置级别设置。 在历程或营销活动中创作电子邮件时，作者必须选择电子邮件类型与通信性质匹配的渠道配置。 此分类会告知在投放之前应用同意检查。

### 打开跟踪控件 {#open-tracking}

Adobe Journey Optimizer允许营销人员在单个消息级别控制打开跟踪（即1x1像素）。 在历程或营销策划中创建电子邮件时，消息属性面板中有两个跟踪选项可用：

* **[!UICONTROL 电子邮件打开次数]**：控制电子邮件中是否包含打开跟踪像素。 默认启用此选项。
* **[!UICONTROL 点击电子邮件]**：控制是否跟踪链接点击。 默认情况下，此选项也处于启用状态。

要禁用特定电子邮件的打开跟踪，请在创建邮件时取消选中&#x200B;**[!UICONTROL 电子邮件打开次数]**&#x200B;选项。 禁用后，选项会阻止为该投放收集打开的跟踪数据。 对于发送给法国订阅者的组织，请在实施日期之前查看所有活动历程和营销活动的打开跟踪设置。

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
Clarify whether unchecking "Email opens" fully removes the 1x1 tracking pixel from the delivered HTML, or whether the pixel is still present in the HTML but open data is suppressed at the data processing layer only. The current wording ("prevents open tracking data from being collected") is intentionally neutral. If the pixel is removed: update to state this explicitly. If the pixel remains but data is not processed: reword to make that distinction clear, to avoid misleading customers seeking CNIL compliance.
-->

[了解如何跟踪消息](../email/message-tracking.md)

### 链接级别的跟踪管理 {#link-tracking}

除了每条消息的打开跟踪切换之外，Adobe Journey Optimizer的Email Designer还精确控制要跟踪的URL。 通过使用Email Designer中的“链接”面板，作者可以查看消息中的所有跟踪URL，并单独设置每个链接的跟踪模式。

每个链接的可用跟踪模式包括：

* **已跟踪**：激活对此 URL 的跟踪。
* **选择退出**：将此URL指定为选择退出或退订URL。
* **镜像页面**：将此URL指定为镜像页面链接。
* **从不**：从不为此URL激活跟踪，无论消息级别设置如何。

将特定链接设置为&#x200B;**从不**&#x200B;有助于确保即使启用了消息级跟踪也不会跟踪某些URL。

### 同意捕获和管理 {#consent-management}

Adobe Journey Optimizer通过Adobe Experience Platform (AEP) Consent and Preferences架构处理同意。 同意首选项存储在用户档案级别，并在历程和活动执行期间自动实施。

与电子邮件跟踪相关的关键同意属性包括：

* **`consents.marketing.email.val`**：主电子邮件营销同意字段。 值`y`表示选择加入；`n`表示选择退出。 默认情况下，空值被视为同意（此默认值可在载入时更改）。

### 选择退出和退出机制 {#opt-out}

Adobe Journey Optimizer为订阅者提供多种机制来选择退出通信并管理其偏好设置，所有这些机制均会在Adobe Experience Platform中更新用户档案的同意属性。

**一键式取消订阅（电子邮件标头）**

在电子邮件渠道配置中启用&#x200B;**[!UICONTROL 启用List-Unsubscribe]**&#x200B;选项后，一键式取消订阅URL和邮件地址会自动添加到电子邮件标头。 收件人无需单击电子邮件正文，即可直接选择退出电子邮件客户端。 默认情况下，新渠道配置将启用此选项。

**一键式选择退出（电子邮件正文）**

作者可以使用电子邮件Designer直接在电子邮件内容中插入一键式选择退出链接。 当收件人单击此链接时，他们的偏好设置会立即更新。 选择退出的范围可以是：

* **渠道级别**：选择将配置文件退出该渠道的所有未来电子邮件通信。
* **身份级别**：仅选择退出当前邮件中使用的特定电子邮件地址。

**通过AJO登陆页面访问首选项中心**

Adobe Journey Optimizer的本机登陆页面功能使组织能够构建首选项中心，订阅者可以在其中管理其通信和跟踪首选项。 当订阅者提交偏好设置中心表单时，他们的选择将写回到“同意和偏好设置”字段组中的其AEP配置文件属性。

对于CNIL合规性方案，可以从电子邮件页脚中链接首选项中心登陆页面（与取消订阅链接不同），以便收件人可以独立于订阅状态管理其跟踪首选项。

### 同意处理和执行 {#consent-enforcement}

当收件人通过以上任何机制选择退出时，会发生以下情况：

* 在Adobe Experience Platform中，配置文件的同意属性(`consents.marketing.email.val`)已更新为`n`。
* 该用户档案会立即从历程和营销活动中的未来营销电子邮件发送中排除。
* 选择退出信息存储在AEP Consent Service数据集中。
* Journey Optimizer在每次发送前会在渠道级别执行同意检查，确保已选择退出的用户档案不会接收营销通信。

### 同意政策 {#consent-policies}

组织可以在Adobe Journey Optimizer中创建并执行同意策略，以确保只有符合特定同意标准的配置文件才能接收通信。 同意策略可以通过营销操作与渠道配置关联。

[了解如何使用同意政策](../action/consent.md)

### 禁止列表和重新请求 {#suppression}

Adobe Journey Optimizer会自动管理包含电子邮件地址的禁止列表，从而导致硬退回、软退回或垃圾邮件投诉。 禁止列表上的用户档案将从将来的营销发送中排除。

Journey Optimizer禁止显示REST API提供了对传出消息的更多编程控制，使组织能够通过API管理禁止显示和行为。

<!--
EDITORIAL NOTE – ENGINEERING CONFIRMATION NEEDED before publish:
AJO has no native equivalent of Campaign v8's "lastPixelRefusalDate" field or re-solicitation typology rule. If re-solicitation governance for pixel consent refusal is required, customers would likely need to: (a) create a custom XDM date field to capture the pixel refusal date, and (b) build an AEP audience that filters out profiles where that date falls within the last six months, then use that audience as a suppression filter in campaigns/journeys. Confirm with Engineering: (1) whether this guidance should be included in this article, and (2) whether any native AJO improvements are planned in this area.
-->

### 报表 {#reporting}

Adobe Journey Optimizer的电子邮件报表通过实时报表和Customer Journey Analytics报表提供打开和点击量度。 为邮件禁用&#x200B;**[!UICONTROL 电子邮件打开次数]**&#x200B;跟踪后，将不会收集该投放的打开数据；报告将仅反映点击次数和其他参与信号。

## 文档引用 {#references}

有关Adobe Journey Optimizer中电子邮件跟踪和同意管理的更多信息，请参阅下面的文档。

| 主题 | 文档参考 |
|-------|------------------------|
| 启用和禁用打开跟踪 | [邮件跟踪](../email/message-tracking.md) |
| 电子邮件选择退出管理 | [电子邮件选择退出管理](../email/email-opt-out.md) |
| List-Unsubscribe（电子邮件标头） | [配置List-Unsubscribe](../email/list-unsubscribe.md) |
| 首选项中心登陆页面 | [登陆页用例](../landing-pages/lp-use-cases.md) |
| 同意和选择退出管理 | [管理选择退出](opt-out.md) |
| 同意政策 | [使用同意政策](../action/consent.md) |
| 电子邮件渠道配置 | [配置电子邮件设置](../email/email-settings.md) |
| 禁止列表 | [管理禁止显示列表](../configuration/manage-suppression-list.md) |
