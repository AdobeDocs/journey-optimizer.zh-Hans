---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件选择退出管理
description: 了解如何使用电子邮件管理选择退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# 电子邮件选择退出管理 {#email-opt-out}

要向收件人提供取消订阅接收电子邮件通信的功能，您必须始终包含 **取消订阅链接** 发送给收件人的电子邮件中。 [了解有关隐私和选择退出管理的更多信息](../privacy/opt-out.md)

为此，您可以：

* 插入 **链接到外部登陆页面** 电子邮件，以便用户取消订阅，从您的品牌接收通信。 [了解如何添加外部选择退出链接](#opt-out-external-lp)

* 添加 **一键式选择退出链接** 到电子邮件内容中。 此链接可让您的收件人快速取消订阅您的通信，而无需重定向到需要确认其选择的登陆页面，从而加快取消订阅过程。 [了解如何添加一键单击选择退出链接](#one-click-opt-out)

此外，如果 **[!UICONTROL List-Unsubscribe]** 选项，则随Journey Optimizer发送的相应电子邮件将在电子邮件标题中包含取消订阅链接。 [了解有关在电子邮件标题中选择退出的更多信息](#unsubscribe-header)

>[!NOTE]
>
>营销类型电子邮件必须包含选择退出链接，这对于事务型消息不是必需的。 消息类别(**[!UICONTROL Marketing]** 或 **[!UICONTROL Transactional]**) [通道表面](../configuration/channel-surfaces.md#email-type) （即，消息预设）级别和创建消息时。

## 外部选择退出 {#opt-out-external-lp}

### 添加退订链接 {#add-unsubscribe-link}

您首先需要在消息中添加取消订阅链接。 为此，请执行以下步骤：

1. 构建您自己的退订登陆页面。

1. 将其托管在您选择的第三方系统上。

1. 在历程中创建消息。

1. 选择内容中的文本，并 [插入链接](../email/message-tracking.md#insert-links) 使用上下文工具栏。

   ![](assets/opt-out-insert-link.png)

1. 选择 **[!UICONTROL External Opt-out/Unsubscription]** 从 **[!UICONTROL Link type]** 下拉列表。

   ![](assets/opt-out-link-type.png)

1. 在 **[!UICONTROL Link]** 字段中，将链接粘贴到第三方登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击 **[!UICONTROL Save]**.

### 实施选择退出的API调用 {#opt-out-api}

要在收件人从登陆页面提交其选择时选择退出，您必须实施 **订阅API调用** 至 [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;}以更新相应配置文件的首选项。

此POST调用如下：

端点：platform.adobe.io/journey/imp/consent/preferences

查询参数：

* **params**:包含加密的有效负载
* **sig**:签名
* **pid**:加密的配置文件ID

这三个参数将包含在发送给收件人的第三方登陆页面URL中：

![](assets/opt-out-parameters.png)

标题要求：

* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授权（来自您技术帐户的用户令牌）

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

[!DNL Journey Optimizer] 将使用这些参数通过 [Adobe Developer](https://developer.adobe.com){target=&quot;_blank&quot;} API调用。

### 使用取消订阅链接发送消息 {#send-message-unsubscribe-link}

配置指向登陆页面的取消订阅链接并实施API调用后，即可发送消息。

1. 通过发送包含链接的消息 [历程](../building-journeys/journey.md).

1. 收到消息后，如果收件人单击取消订阅链接，则会显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人提交表单(此处为通过点击 **取消订阅** 按钮)，则用户档案数据将通过 [API调用](#opt-out-api).

1. 然后，已选择退出的收件人将被重定向到确认消息屏幕，指示已成功退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，该用户将不会收到来自您品牌的通信，除非再次订阅。

1. 要检查相应配置文件的选择是否已更新，请转到Experience Platform，然后通过选择身份命名空间和相应的身份值来访问配置文件。 在 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}。

   ![](assets/opt-out-profile-choice.png)

   在 **[!UICONTROL Attributes]** 选项卡，您可以看到 **[!UICONTROL choice]** 已更改为 **[!UICONTROL no]**.

## 一键单击选择退出 {#one-click-opt-out}

要在电子邮件中添加选择退出链接，请执行以下步骤。

1. [插入链接](../email/message-tracking.md#insert-links) 选择 **[!UICONTROL One click Opt-out]** 作为链接类型。

   ![](assets/message-tracking-opt-out.png)

1. 选择您希望如何应用选择退出：在渠道、身份或订阅级别。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL Channel]**:选择退出适用于将来发送到当前渠道用户档案目标（即电子邮件地址）的消息。 如果多个目标与某个用户档案关联，则选择退出将应用于该渠道配置文件中的所有目标（即电子邮件地址）。
   * **[!UICONTROL Identity]**:选择退出适用于发送给当前消息所使用的特定目标（即电子邮件地址）的将来消息。
   * **[!UICONTROL Subscription]**:选择退出适用于与特定订阅列表关联的未来消息。 仅当当前消息与订阅列表关联时，才能选择此选项。

1. 输入退订后用户将被重定向的登陆页面的URL。 此页面仅用于确认选择退出是否成功。

   >[!NOTE]
   >
   >如果您启用了 **列表取消订阅** 选项，当用户单击电子邮件标题中的取消订阅链接时，也会使用此URL。 [了解更多](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以个性化您的链接。 在中了解有关个性化URL的更多信息 [此部分](../personalization/personalization-syntax.md).

1. 保存更改。

通过 [历程](../building-journeys/journey.md)，则当收件人单击选择退出链接时，其用户档案会立即被选择退出。

## 电子邮件标题中的取消订阅链接 {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="向电子邮件标题添加取消订阅链接"
>abstract="启用List-Unsubscribe以添加指向电子邮件标题的取消订阅链接。 要设置取消订阅URL，请在电子邮件内容中插入一个单击选择退出链接。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#one-click-opt-out" text="一键单击选择退出"

如果 [“列表取消订阅”选项](../configuration/channel-surfaces.md#list-unsubscribe) 在渠道表面级别启用， [!DNL Journey Optimizer] 将在电子邮件标题中包含取消订阅链接。

例如，取消订阅链接在Gmail中将如下所示：

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>要在电子邮件标题中显示取消订阅链接，收件人的电子邮件客户端必须支持此功能。

取消订阅地址是默认地址 **[!UICONTROL Mailto (unsubscribe)]** 地址显示在相应的通道表面中。 [了解更多](../configuration/channel-surfaces.md#list-unsubscribe).

要设置个性化的取消订阅URL，请在电子邮件内容中插入一键单击的选择退出链接，然后输入您选择的URL。 [了解更多](#one-click-opt-out)

根据电子邮件客户端的不同，单击标题中的取消订阅链接可能会产生以下影响：

* 取消订阅请求将发送到默认的取消订阅地址。

* 收件人会被定向到您在向消息添加选择退出链接时指定的登陆页面URL。

   >[!NOTE]
   >
   >如果您没有在消息内容中添加一键单击选择退出链接，则不会显示登陆页面。

* 相应的用户档案会立即退出，并在Experience Platform中更新此选择。 在 [Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html#getting-started){target=&quot;_blank&quot;}。
