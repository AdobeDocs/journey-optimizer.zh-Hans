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
source-git-commit: fb14db58f9facac87e83a85e8f163ea31732a374
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 23%

---

# 电子邮件选择退出管理 {#email-opt-out}

在从历程或活动发送消息时，必须始终确保客户可以取消订阅未来的通信。取消订阅后，用户档案将自动从未来营销消息的受众中删除。  [了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

>[!NOTE]
>
>您的所有营销消息必须包含选择退出链接。 对于事务型消息，这不是必需的。 消息类别 — **[!UICONTROL 营销]**&#x200B;或&#x200B;**[!UICONTROL 事务性]** — 在[渠道配置](../configuration/channel-surfaces.md#email-type)级别和创建消息时定义。

要在电子邮件内容中插入退订链接，您可以：

* 在电子邮件标头中添加一键式取消订阅URL。 渠道配置级别的&#x200B;**[!UICONTROL 启用List-Unsubscribe]**&#x200B;选项为电子邮件标头添加了选择退出链接。 [在电子邮件标头中了解有关选择退出的更多信息](#unsubscribe-header)

* 为您的电子邮件启用&#x200B;**一键式选择退出链接**。  [了解如何添加一键式选择退出链接](#one-click-opt-out)

* 插入指向登陆页面&#x200B;**的**&#x200B;链接。 [了解如何添加选择退出登陆页面](#opt-out-external-lp)


## 一步式选择退出 {#opt-out-one-step}

### 电子邮件标头中的一键取消订阅 URL {#unsubscribe-header}

<!--Do not modify - Legal Review Done -->

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="向电子邮件标头添加取消订阅URL"
>abstract="启用List-Unsubscribe以向电子邮件标头添加取消订阅URL。 要在消息中设置取消订阅URL，请在电子邮件内容中插入一键式选择退出链接。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/channels/email/email-opt-out#one-click-opt-out" text="一键式选择退出电子邮件内容"

一键式列表取消订阅URL是电子邮件发件人信息旁边显示的取消订阅链接或按钮，收件人只需单击一下即可立即选择退出您的邮件列表。 在Adobe Journey Optimizer中，当打开&#x200B;**启用List-Unsubscribe**&#x200B;选项时，电子邮件标头将同时包含邮件和/或URL，默认情况下，收件人可以使用这些URL取消订阅您的邮件列表。

必须在渠道配置级别激活[启用列表取消订阅](email-settings.md#list-unsubscribe)切换开关，以便使用此配置的电子邮件在电子邮件标头中包含一键式取消订阅URL。

>[!NOTE]
>
>要在电子邮件标头中显示一键式取消订阅URL，收件人的电子邮件客户端必须支持此功能。


例如，一键式取消订阅URL会在Gmail中显示类似以下的取消订阅链接：

![](assets/unsubscribe-header.png)


借助Adobe Journey Optimizer，您可以配置电子邮件配置设置，在电子邮件标题中使用自动生成的一键式取消订阅URL和邮寄地址，或者在电子邮件正文中包含一键式选择退出URL：当收件人单击一键式选择退出链接时，收件人的取消订阅请求会得到相应处理。

<!--
>[!AVAILABILITY]
>
>One-click Unsubscribe URL Header will be available in Adobe Journey Optimizer starting June 3, 2024.
>
-->

根据电子邮件客户端和[电子邮件配置取消订阅设置](email-settings.md#list-unsubscribe)的不同，单击电子邮件标头中的取消订阅链接可能会产生以下影响：

* 在您启用&#x200B;**Mailto（取消订阅）**&#x200B;功能后，将根据您创建的子域将取消订阅请求发送到默认的取消订阅地址。
* 当您启用&#x200B;**一键式取消订阅URL**&#x200B;功能时，或者如果您在电子邮件正文内容中插入了取消订阅URL，则当收件人单击一键式取消订阅URL（基于您创建的子域）时，收件人会直接在渠道级别或ID级别（取决于同意的设置方式）选择退出。

在这两种情况下，收件人的相应用户档案会立即退出订阅，并且此选择将在Experience Platform中更新。 请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}以了解详情。

如果您在列表取消订阅标头中切换了&#x200B;**[!UICONTROL 启用List-Unsubscribe]**&#x200B;选项，我们建议您同时启用这两种方法 — **Mailto（取消订阅）**&#x200B;和&#x200B;**一键单击取消订阅URL**。 并非所有电子邮件客户端都支持HTTP方法。 利用提供的Mailto list-unsubscribe功能，您可以选择替代方案，可以更好地保护发件人的信誉，并且所有收件人都能够使用取消订阅功能。 [了解详情](email-settings.md#list-unsubscribe)


### 一键式选择退出电子邮件内容 {#one-click-opt-out}

要设置个性化的取消订阅URL，请在电子邮件内容中插入一键式选择退出链接，然后输入您选择的URL，如下所述：

1. 访问您的电子邮件内容并[插入链接](../email/message-tracking.md#insert-links)。
1. 选择&#x200B;**[!UICONTROL 一次单击退出]**&#x200B;作为链接类型。

   ![](assets/message-tracking-opt-out.png)

1. 输入用户取消订阅后重定向到的登陆页面的URL。 此页用于确认选择退出是否成功。

   >[!NOTE]
   >
   >如果在[渠道配置级别](email-settings.md#list-unsubscribe)启用了&#x200B;**[!UICONTROL List-Unsubscribe]**&#x200B;选项，并且取消选中了默认的一键式选择退出URL选项，则当用户单击电子邮件标头中的取消订阅链接时，将使用此URL。 [了解详情](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以个性化自己的链接。在[本节](../personalization/personalization-syntax.md)中了解更多关于个性化 URL 的信息。

1. 选择您要应用选择退出的层级：渠道、身份标识或订阅。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 渠道]**：选择退出适用于将来发送到当前渠道的轮廓目标（即电子邮件地址）的消息。如果多个目标与一个轮廓关联，则选择退出适用于该渠道的轮廓中的所有目标（即电子邮件地址）。
   * **[!UICONTROL 身份标识]**：选择退出适用于在将来发送给当前消息所使用的特定目标（即电子邮件地址）的消息。
     <!--* **[!UICONTROL Subscription]**: The opt-out applies to future messages associated with a specific subscription list. This option can only be selected if the current message is associated with a subscription list.-->

1. 保存更改。


## 两步式选择退出 {#opt-out-external-lp}

标准选择退出机制依赖于两个步骤：订阅者单击电子邮件中的选择退出链接，然后被重定向到选择退出登陆页面，以确认取消订阅。

要实施此退订模式，您必须创建和发布选择退出登陆页面，并在电子邮件中添加退订链接，其中含有指向登陆页面的链接。 这些步骤概述如下。


### 先决条件 {#prereq-lp}

要设置两步式选择退出机制，您必须创建自己的退订登陆页面。 第一个登陆页面将从您的消息中链接，并且必须包含行动号召按钮。 用户单击按钮时，将显示确认消息。

在[此页面](../landing-pages/lp-use-cases.md#opt-out)中了解如何在Adobe Journey Optimizer中创建登陆页面以管理退订。

您还可以使用外部登陆页面。 在这种情况下，请配置API以在收件人取消订阅时将信息发送到Adobe Journey Optimizer。

+++ 了解如何实施选择退出API调用

要在收件人从登陆页面提交选择时为其完成选择退出，您必须通过[Adobe Developer](https://developer.adobe.com){target="_blank"}实施&#x200B;**订阅API调用**&#x200B;以更新相应用户档案的偏好设置。

此 POST 调用如下：

端点：https://platform.adobe.io/journey/imp/consent/preferences

查询参数：

* **params**：包含加密后的有效负载
* **pid**：加密后的轮廓 ID

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

[!DNL Journey Optimizer]使用这些参数通过[Adobe Developer](https://developer.adobe.com){target="_blank"} API调用更新相应用户档案的选择。

+++


### 添加取消订阅链接 {#add-unsubscribe-link}

您首先需要在消息中添加取消订阅链接。为此，请执行以下步骤：

1. 创建消息并使用上下文工具栏[插入链接](../email/message-tracking.md#insert-links)。

   ![](assets/opt-out-insert-link.png)

1. 从&#x200B;**[!UICONTROL 类型]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 登陆页面]**，然后在&#x200B;**[!UICONTROL 登陆页面]**&#x200B;字段中选择您的选择退出登陆页面。

   如果您使用的是外部登陆页面，请从&#x200B;**[!UICONTROL 类型]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 外部选择退出/退订]**。

   ![](assets/opt-out-link-type.png)

   在&#x200B;**[!UICONTROL 链接]**&#x200B;字段中，将链接粘贴到您的第三方登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。


### 使用取消订阅链接发送消息 {#send-message-unsubscribe-link}

配置指向登陆页面的取消订阅链接后，您可以创建和发送消息。

1. 使用退订链接配置消息，并将其发送给订阅者。

1. 收到消息后，如果收件人单击取消订阅链接，则会显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人提交了表单 — 在此处，通过点击登陆页面中的&#x200B;**[!UICONTROL Unsubscribe]**&#x200B;按钮 — 将通过API调用更新用户档案数据。

1. 然后，选择退出的收件人将被重定向至确认消息屏幕，提示收件人选择退出已成功完成。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次订阅，否则这个用户将不会收到来自您的品牌的通信。

1. 要检查相应轮廓的选择是否已更新，请转到 Experience Platform，并通过选择身份标识命名空间和相应的身份标识值访问该轮廓。请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}以了解详情。

   ![](assets/opt-out-profile-choice.png)

   在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，您可以看到&#x200B;**[!UICONTROL 选择]**&#x200B;的值已更改为&#x200B;**[!UICONTROL 否]**。

