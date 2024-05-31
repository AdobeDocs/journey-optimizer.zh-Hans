---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件选择退出管理
description: 了解如何通过电子邮件管理选择退出
feature: Email Design, Privacy
topic: Content Management
role: User
level: Intermediate
keywords: 选择退出、电子邮件、链接、取消订阅
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: fb6a2e29f92e4b7e65eb495a654960e3249f9508
workflow-type: tm+mt
source-wordcount: '1350'
ht-degree: 26%

---

# 电子邮件选择退出管理 {#email-opt-out}

在从历程或活动发送消息时，必须始终确保客户可以取消订阅未来的通信。取消订阅后，用户档案将自动从未来营销消息的受众中删除。  [了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

>[!NOTE]
>
>您的所有营销消息必须包含选择退出链接。 对于事务型消息，这不是必需的。 消息类别 —  **[!UICONTROL 营销]** 或 **[!UICONTROL 事务性]**  — 定义于 [渠道表面](../configuration/channel-surfaces.md#email-type) 级别和创建消息时。

要在电子邮件内容中插入退订链接，您可以：

* 在电子邮件标头中添加一键式取消订阅URL。 启用 **[!UICONTROL 列表取消订阅标头]** 渠道平面级别的选项在电子邮件标题中添加了一个选择退出链接。 [了解有关电子邮件标题中选择退出的更多信息](#unsubscribe-header)

* 启用 **一键式选择退出链接** 用于电子邮件。  [了解如何添加一键式选择退出链接](#one-click-opt-out)

* 插入 **链接到登陆页面**. [了解如何添加选择退出登陆页面](#opt-out-external-lp)

## 一步式选择退出 {#opt-out-one-step}

### 在电子邮件标头中一键单击取消订阅URL {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="在电子邮件标头中添加取消订阅URL"
>abstract="启用List-Unsubscribe标头，以便在电子邮件标头中添加取消订阅URL。 要设置取消订阅 URL，请在电子邮件内容中插入一个一键式选择退出链接。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hans#one-click-opt-out" text="一键式选择退出"

一键式列表取消订阅URL是电子邮件发件人信息旁边显示的取消订阅链接或按钮，收件人只需单击一下即可立即选择退出您的邮件列表。 在Adobe Journey Optimizer中，当 **启用List-Unsubscribe** 选项已切换，默认情况下，电子邮件标头包括邮件和/或URL，收件人可以使用它们取消订阅您的邮件列表。

此 [启用List-Unsubscribe](email-settings.md#list-unsubscribe) 必须在渠道平面级别激活切换，以便使用此表面的电子邮件在电子邮件标头中包含一键式取消订阅URL。

>[!NOTE]
>
>要在电子邮件标头中显示一键式取消订阅URL，收件人的电子邮件客户端必须支持此功能。


例如，一键式取消订阅URL会在Gmail中显示类似以下的取消订阅链接：

![](assets/unsubscribe-header.png)


借助Adobe Journey Optimizer，您可以在电子邮件标题中使用自动生成的一键式取消订阅URL和邮件地址配置电子邮件界面设置，或者在电子邮件正文中包含一键式选择退出URL：当收件人单击一键式选择退出链接时，收件人的取消订阅请求会得到相应处理。

>[!AVAILABILITY]
>
>从2024年6月3日开始，在Adobe Journey Optimizer中将提供一键式取消订阅URL标头。
>

根据电子邮件客户端和 [电子邮件表面取消订阅设置](email-settings.md#list-unsubscribe)，单击电子邮件标头中的取消订阅链接可能会产生以下影响：

* 当 **Mailto（取消订阅）** 功能由您启用，取消订阅请求将根据您创建的子域发送到默认的取消订阅地址。
* 当 **一键式取消订阅URL** 功能由您启用 — 或者如果您在电子邮件正文内容中插入了取消订阅URL — 当收件人单击基于您创建的子域的一键式取消订阅URL时，收件人会直接在渠道级别或ID级别（取决于同意的设置方式）选择退出。

在这两种情况下，收件人的相应用户档案会立即退出订阅，并且此选择将在Experience Platform中更新。 在中了解详情 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}.

如果您已经为List Unsubscribe标头切换了Enable-In ，我们建议您启用Mailto和One-Click&amp; Unsubscribe URL这两个功能方法。 并非所有电子邮件客户端都支持HTTP方法。 使用为您提供用于选择替代项的Mailto list-unsubscribe功能，可以更好地保护您的发件人信誉，并且您的所有收件人都有权使用取消订阅功能。 [了解详情](email-settings.md#list-unsubscribe)


### 一键式选择退出电子邮件内容 {#one-click-opt-out}

要设置个性化的取消订阅URL，请在电子邮件内容中插入一键式选择退出链接，然后输入您选择的URL，如下所述：

1. 访问您的电子邮件内容并 [插入链接](../email/message-tracking.md#insert-links).
1. 选择 **[!UICONTROL 一键选择退出]** 作为链接类型。

   ![](assets/message-tracking-opt-out.png)

1. 输入用户取消订阅后重定向到的登陆页面的URL。 此页用于确认选择退出是否成功。

   >[!NOTE]
   >
   >如果您已启用 **[!UICONTROL 列表 — 取消订阅]** 位于以下位置的选项： [渠道表面级别](email-settings.md#list-unsubscribe) 并取消选中默认的一键式选择退出URL选项，则当用户单击电子邮件标头中的取消订阅链接时，将使用此URL。 [了解详情](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以个性化自己的链接。在[本节](../personalization/personalization-syntax.md)中了解更多关于个性化 URL 的信息。

1. 选择您要应用选择退出的层级：渠道、身份或订阅。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 渠道]**：选择退出适用于将来发送到当前渠道的用户档案目标（即电子邮件地址）的消息。如果多个目标与一个用户档案关联，则选择退出适用于该渠道的用户档案中的所有目标（即电子邮件地址）。
   * **[!UICONTROL 标识]**：选择退出适用于在将来发送给当前消息所使用的特定目标（即电子邮件地址）的消息。
   * **[!UICONTROL 订阅]**：选择退出适用于与特定订阅列表关联的将来发送的消息。仅在当前消息与订阅列表关联时，才能选择此选项。

1. 保存更改。



## 两步式选择退出 {#opt-out-external-lp}

标准选择退出机制依赖于两个步骤：订阅者单击电子邮件中的选择退出链接，然后被重定向到选择退出登陆页面，以确认取消订阅。

要实施此退订模式，您必须创建和发布选择退出登陆页面，并在电子邮件中添加退订链接，其中含有指向登陆页面的链接。 这些步骤概述如下。


### 先决条件 {#prereq-lp}

要设置两步式选择退出机制，您必须创建自己的退订登陆页面。 第一个登陆页面将从您的消息中链接，并且必须包含行动号召按钮。 用户单击按钮时，将显示确认消息。

了解如何在Adobe Journey Optimizer中创建登陆页面以管理中的退订 [此页面](../landing-pages/lp-use-cases.md#opt-out).

您还可以使用外部登陆页面。 在这种情况下，请配置API以在收件人取消订阅时将信息发送到Adobe Journey Optimizer。

+++ 了解如何实施选择退出API调用

要在收件人从登陆页面提交选择时为其完成选择退出，您必须实施 **订阅API调用** 到 [Adobe Developer](https://developer.adobe.com){target="_blank"} 以更新相应用户档案的偏好设置。

此 POST 调用如下：

端点：https://platform.adobe.io/journey/imp/consent/preferences

查询参数：

* **params**：包含加密后的有效负载
* **pid**：加密后的用户档案 ID

以上三个参数将包含在发送给您的收件人的第三方登陆页面 URL 中：

![](assets/opt-out-parameters.png)

标头要求：

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授权（技术帐户中的用户令牌）

请求正文：

```
{
   "marketing": [
       {
            "type": "email",           
            "choice": "no",          
            "scope": "channel"       
        }
    ],
 
}
```

[!DNL Journey Optimizer] 使用这些参数更新相应用户档案的选择 [Adobe Developer](https://developer.adobe.com){target="_blank"} API调用。

+++


### 添加取消订阅链接 {#add-unsubscribe-link}

您首先需要在消息中添加取消订阅链接。为此，请执行以下步骤：

1. 创建消息并 [插入链接](../email/message-tracking.md#insert-links) 使用上下文工具栏。

   ![](assets/opt-out-insert-link.png)

1. 选择 **[!UICONTROL 登陆页面]** 从 **[!UICONTROL 类型]** 下拉列表中，选择您的选择退出登陆页面 **[!UICONTROL 登陆页面]** 字段。

   如果您使用的是外部登陆页面，请选择 **[!UICONTROL 外部选择退出/退订]** 从 **[!UICONTROL 类型]** 下拉列表。

   ![](assets/opt-out-link-type.png)

   在&#x200B;**[!UICONTROL 链接]**&#x200B;字段中，将链接粘贴到您的第三方登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。


### 使用取消订阅链接发送消息 {#send-message-unsubscribe-link}

配置指向登陆页面的取消订阅链接后，您可以创建和发送消息。

1. 使用退订链接配置消息，并将其发送给订阅者。

1. 收到消息后，如果收件人单击取消订阅链接，则会显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人提交了表单 — 在此处，通过点击 **[!UICONTROL 取消订阅]** 按钮 — 通过API调用更新用户档案数据。

1. 然后，选择退出的收件人将被重定向至确认消息屏幕，提示收件人选择退出已成功完成。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次订阅，否则这个用户将不会收到来自您的品牌的通信。

1. 要检查相应用户档案的选择是否已更新，请转到 Experience Platform，并通过选择身份命名空间和相应的身份值访问该用户档案。在中了解详情 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，您可以看到&#x200B;**[!UICONTROL 选择]**&#x200B;的值已更改为&#x200B;**[!UICONTROL 否]**。

