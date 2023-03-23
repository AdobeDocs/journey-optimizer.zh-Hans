---
solution: Journey Optimizer
product: journey optimizer
title: 配置电子邮件设置
description: 了解如何在渠道表面级别配置电子邮件设置
feature: Surface
topic: Administration
role: Admin
level: Intermediate
keywords: 设置，电子邮件，配置
exl-id: 13536962-7541-4eb6-9ccb-4f97e167734a
source-git-commit: 9657862f1c6bdb2399fcf3e6384bb9dec5b8f32b
workflow-type: tm+mt
source-wordcount: '1652'
ht-degree: 9%

---

# 配置电子邮件设置 {#email-settings}

要开始创建电子邮件，您需要设置电子邮件渠道界面，以定义消息所需的所有技术参数。 [了解如何创建曲面](../configuration/channel-surfaces.md)

在渠道表面配置的专用部分中定义电子邮件设置。

![](assets/preset-email-settings.png)

将按照以下逻辑选取用于发送通信的电子邮件界面配置：

* 对于批处理和拆分历程，它不适用于在进行电子邮件表面配置之前已启动的批处理或拆分执行。 更改将在下次重复或新执行时被提取。

* 对于事务型消息，将立即接收更改，以便进行下次通信（最长为五分钟延迟）。

>[!NOTE]
>
>更新的电子邮件界面设置将在历程或使用该界面的营销活动中自动选取。

## 电子邮件类型 {#email-type}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_emailtype"
>title="定义电子邮件类别"
>abstract="选择使用此表面时将发送的电子邮件类型：营销性的促销电子邮件，此时需要用户同意；或者事务性的非商业电子邮件，此时在特定上下文中，也可以发送到未订阅的配置文件。"

在 **电子邮件类型** 部分，选择将随曲面一起发送的消息类型： **营销** 或 **事务型**.

* 选择 **营销** 对于促销电子邮件：这些消息需要用户同意。

* 选择 **事务型** 例如，用于订单确认、密码重置通知或投放信息等非商业电子邮件。

>[!CAUTION]
>
>**事务型** 可向取消订阅营销通信的用户档案发送电子邮件。 这些消息只能在特定上下文中发送。

创建消息时，必须选择与您为电子邮件选择的类别匹配的有效渠道表面。

## 子域和IP池 {#subdomains-and-ip-pools}

在 **子域和IP池** 部分，您必须：

1. 选择要用于发送电子邮件的子域。 [了解详情](../configuration/about-subdomain-delegation.md)

1. 选择要与曲面关联的IP池。 [了解详情](../configuration/ip-pools.md)

![](assets/preset-subdomain-ip-pool.png)

当选定的IP池位于 [版本](../configuration/ip-pools.md#edit-ip-pool) (**[!UICONTROL 处理]** 状态)且从未与选定的子域关联。 否则，仍将使用IP池/子域关联的最旧版本。 如果出现这种情况，请将曲面另存为草稿，并在IP池具有 **[!UICONTROL 成功]** 状态。

>[!NOTE]
>
>对于非生产环境，Adobe不会创建现成的测试子域，也不会授予对共享发送IP池的访问权限。 您需要 [委派您自己的子域](../configuration/delegate-subdomain.md) 并使用分配给贵组织的池中的IP。

选择IP池后，当将鼠标悬停在IP池下拉列表下方显示的IP地址上时，将显示PTR信息。 [了解有关PTR记录的更多信息](../configuration/ptr-records.md)

![](assets/email-surface-ptr-record.png)

>[!NOTE]
>
>如果未配置PTR记录，请联系您的Adobe代表。

## 列表取消订阅 {#list-unsubscribe}

On [选择子域](#subdomains-and-ip-pools) 在列表中， **[!UICONTROL 启用列表取消订阅]** 选项。

![](assets/preset-list-unsubscribe.png)

默认启用选项。

如果保持启用状态，则取消订阅链接将自动包含在电子邮件标题中，例如：

![](assets/preset-list-unsubscribe-header.png)

如果禁用此选项，则电子邮件标题中不会显示取消订阅链接。

取消订阅链接包含两个元素：

* 安 **取消订阅电子邮件地址**，所有取消订阅请求都将发送到该服务器。

   在 [!DNL Journey Optimizer]，则取消订阅电子邮件地址为默认地址 **[!UICONTROL Mailto（取消订阅）]** 通道表面中显示的地址，基于 [选定子域](#subdomains-and-ip-pools).

   ![](assets/preset-list-unsubscribe-mailto.png)

* 的 **取消订阅URL**，取消订阅后，用户将被重定向到的登陆页面的URL。

   如果您添加 [一键式选择退出链接](../privacy/opt-out.md#one-click-opt-out) 对于使用此表面创建的消息，取消订阅URL将是为一键单击选择退出链接定义的URL。

   ![](assets/preset-list-unsubscribe-opt-out-url.png)

   >[!NOTE]
   >
   >如果您没有在消息内容中添加一键单击选择退出链接，则不会向用户显示登陆页面。

在 [此部分](../privacy/opt-out.md#unsubscribe-header).

<!--Select the **[!UICONTROL Custom List-Unsubscribe]** option to enter your own Unsubscribe URL and/or your own Unsubscribe email address.(to add later)-->

## 标头参数 {#email-header}

在 **[!UICONTROL 标头参数]** 部分，输入与使用该表面发送的电子邮件类型关联的发件人名称和电子邮件地址。

* **[!UICONTROL 发件人名称]**:发件人的名称，如您的品牌名称。

* **[!UICONTROL 发件人电子邮件]**:要用于通信的电子邮件地址。

* **[!UICONTROL 回复（名称）]**:收件人单击 **回复** 按钮。

* **[!UICONTROL 回复（电子邮件）]**:收件人单击 **回复** 按钮。 [了解详情](#reply-to-email)

* **[!UICONTROL 错误电子邮件]**:收到ISP在收到几天邮件后（异步退回）生成的所有错误，均位于此地址。

>[!CAUTION]
>
>的 **[!UICONTROL 发件人电子邮件]** 和 **[!UICONTROL 错误电子邮件]** 地址必须使用当前选定的 [委派子域](../configuration/about-subdomain-delegation.md). 例如，如果委派的子域为 *marketing.luma.com*，您可以使用 *contact@marketing.luma.com* 和 *error@marketing.luma.com*.

![](assets/preset-header.png)

>[!NOTE]
>
>地址必须以字母(A-Z)开头，且只能包含字母数字字符。 还可以使用下划线 `_`，点`.` 和连字符 `-` 字符。

### 回复电子邮件 {#reply-to-email}

定义 **[!UICONTROL 回复（电子邮件）]** 地址，您可以指定任何电子邮件地址（如果地址是有效地址），且格式正确且没有任何类型。

为确保正确的回复管理，请遵循以下建议：

* 用于回复的收件箱将收到所有回复电子邮件，包括外出通知和质询响应，因此，请确保您已经完成手动或自动流程，以处理登陆此收件箱的电子邮件。

* 确保专用收件箱具有足够的接收容量，可接收使用电子邮件界面发送的所有回复电子邮件。 如果收件箱返回退回，则可能未收到客户的某些回复。

* 处理回复时必须牢记隐私和合规义务，因为它们可能包含个人身份信息(PII)。

* 请勿在回复收件箱中将邮件标记为垃圾邮件，因为这会影响发送到此地址的所有其他回复。

此外，在定义 **[!UICONTROL 回复（电子邮件）]** 地址，请确保使用具有有效MX记录配置的子域，否则电子邮件表面处理将失败。

如果您在提交电子邮件界面时遇到错误，则表示未为您输入的地址的子域配置MX记录。 请联系您的管理员以配置相应的MX记录或使用其他具有有效MX记录配置的地址。

>[!NOTE]
>
>如果您输入的地址的子域是 [充分授权](../configuration/delegate-subdomain.md#full-subdomain-delegation) 要Adobe，请联系您的Adobe客户经理。

### 转发电子邮件 {#forward-email}

如果您希望将收到的所有电子邮件转发到特定电子邮件地址 [!DNL Journey Optimizer] 对于委派的子域，请联系Adobe客户关怀团队。 您需要提供：

* 您选择的转发电子邮件地址。 请注意，转发电子邮件地址域与委派给Adobe的任何子域都不匹配。
* 您的沙盒名称。
* 将使用转发电子邮件地址的表面名称。
* 当前 **[!UICONTROL 回复（电子邮件）]** 在通道表面级别设置的地址。

>[!NOTE]
>
>每个子域只能有一个转发电子邮件地址。 因此，如果多个曲面使用相同的子域，则所有这些子域都必须使用相同的转发电子邮件地址。

转发电子邮件地址将由Adobe设置。 这可能需要3到4天。

## 密送电子邮件 {#bcc-email}

您可以发送由发送的电子邮件的相同副本（或盲文副本） [!DNL Journey Optimizer] 发送到密件抄送收件箱，以供符合要求或进行存档。

为此，请启用 **[!UICONTROL 密送电子邮件]** 通道曲面级别的可选功能。 [了解详情](../configuration/archiving-support.md#bcc-email)

![](assets/preset-bcc.png)

此外，在定义 **[!UICONTROL 密送电子邮件]** 地址，请确保使用具有有效MX记录配置的子域，否则电子邮件表面处理将失败。

如果您在提交电子邮件界面时遇到错误，则表示未为您输入的地址的子域配置MX记录。 请联系您的管理员以配置相应的MX记录或使用其他具有有效MX记录配置的地址。

## 电子邮件重试参数 {#email-retry}

>[!CONTEXTUALHELP]
>id="ajo_admin_presets_retryperiod"
>title="调整重试时段"
>abstract="当电子邮件投放由于临时软退回错误失败时，将重试 3.5 天（84 小时）。您可以调整此默认重试时段以更好地满足您的需求。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/monitor-reputation/retries.html" text="关于重试"

您可以配置 **电子邮件重试参数**.

![](assets/preset-retry-parameters.png)

默认情况下， [重试时段](../configuration/retries.md#retry-duration) 设置为84小时，但您可以根据自己的需求调整此设置。

您必须在以下范围内输入整数值（以小时或分钟为单位）：

* 对于营销电子邮件，最短重试期限为6小时。
* 对于事务型电子邮件，最短重试期限为10分钟。
* 对于这两种电子邮件类型，最大重试时间段为84小时（或5040分钟）。

了解有关重试的更多信息(位于 [此部分](../configuration/retries.md).

## URL跟踪 {#url-tracking}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_utm"
>title="定义 URL 跟踪参数"
>abstract="使用此部分可自动将跟踪参数附加到在电子邮件内容中提供的 URL。此功能属于可选功能。"

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_url_preview"
>title="预览 URL 跟踪参数"
>abstract="查看如何对电子邮件内容中出现的 URL 附加跟踪参数。"

您可以使用 **[!UICONTROL URL跟踪参数]** 来衡量您跨渠道营销工作的有效性。 此功能属于可选功能。

此部分中定义的参数将附加到电子邮件内容中包含的URL的末尾。 然后，您可以在Web分析工具(如Adobe Analytics或Google Analytics)中捕获这些参数，并创建各种性能报表。

<!--Three URL tracking parameters are auto-populated as an example when you create a channel surface. You can edit these and add up to 10 tracking parameters using the **[!UICONTROL Add new parameter]** button.-->

您最多可以使用 **[!UICONTROL 添加新参数]** 按钮。

![](assets/preset-url-tracking.png)

要配置URL跟踪参数，您可以直接在 **[!UICONTROL 名称]** 和 **[!UICONTROL 值]** 字段。

<!--You can also choose from a list of predefined values by navigating to the following objects:
* Journey attributes: **Source id**, **Source name**, **Source version id**
* Action attributes: **Action id**, **Action name**
* Offer decisioning attributes: **Offer id**, **Offer name**

![](assets/preset-url-tracking-source.png)

>[!CAUTION]
>
>Do not select a folder: make sure to browse to the necessary folder and select a profile attribute to use as a tracking parameter value.-->

您还可以编辑每个 **[!UICONTROL 值]** 字段 [表达式编辑器](../personalization/personalization-build-expressions.md). 单击编辑图标以打开编辑器。 从此处，您可以选择所选的上下文属性和/或直接编辑文本。

![](assets/preset-url-tracking-editor.png)

>[!NOTE]
>
>您可以结合使用表达式编辑器中的上下文属性和键入文本值。 每个 **[!UICONTROL 值]** 字段可包含最多5 KB的字符数。

<!--You can drag and drop the parameters to reorder them.-->

以下是与Adobe Analytics和Google Analytics兼容的URL的示例。

* Adobe Analytics兼容URL: `www.YourLandingURL.com?cid=email_AJO_{{context.system.source.id}}_image_{{context.system.source.name}}`

* Google Analytics兼容URL: `www.YourLandingURL.com?utm_medium=email&utm_source=AJO&utm_campaign={{context.system.source.id}}&utm_content=image`

您可以动态预览生成的跟踪URL。 每次添加、编辑或删除参数时，预览都会自动更新。

![](assets/preset-url-tracking-preview.png)