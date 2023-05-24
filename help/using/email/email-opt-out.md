---
solution: Journey Optimizer
product: journey optimizer
title: 电子邮件选择退出管理
description: 瞭解如何透過電子郵件管理選擇退出
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 選擇退出，電子郵件，連結，取消訂閱
exl-id: 4bb51bef-5dab-4a72-8511-1a5e528f4b95
source-git-commit: cda4c1d88fedc75c7fded9971e45fdc9740346c4
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 79%

---

# 电子邮件选择退出管理 {#email-opt-out}

為了讓收件者提供取消訂閱接收電子郵件通訊的功能，您必須一律包含 **取消訂閱連結** 每封寄給收件者的電子郵件中。 [進一步瞭解隱私權與選擇退出管理](../privacy/opt-out.md)

若要這麼做，您可以：

* 插入 **外部登陸頁面的連結** 加入電子郵件，讓使用者能夠取消訂閱來自您品牌的通訊。 [瞭解如何新增外部選擇退出連結](#opt-out-external-lp)

* 新增 **一鍵選擇退出連結** 放入您的電子郵件內容。 该链接可让您的收件人快速取消订阅您的通信，而无需重定向到需要确认其选择的登陆页面，从而简化取消订阅流程。 [瞭解如何新增一鍵選擇退出連結](#one-click-opt-out)

此外，如果 **[!UICONTROL 清單 — 取消訂閱]** 選項在頻道介面層級啟用，透過Journey Optimizer傳送的對應電子郵件將在電子郵件標題中包含取消訂閱連結。 [進一步瞭解電子郵件標頭中的選擇退出](#unsubscribe-header)

>[!NOTE]
>
>营销类型电子邮件必须包含选择退出链接，这对于事务型邮件不是必需的。訊息類別(**[!UICONTROL 行銷]** 或 **[!UICONTROL 異動]**)定義於 [管道表面](../configuration/channel-surfaces.md#email-type) （即訊息預設集）層級，以及在建立訊息時)。

## 外部选择退出 {#opt-out-external-lp}

### 添加取消订阅链接 {#add-unsubscribe-link}

您首先需要在消息中添加取消订阅链接。为此，请执行以下步骤：

1. 构建自己的退订登陆页面。

1. 在您选择的第三方系统上托管它。

1. 在历程中创建消息。

1. 在内容中选择文本，然后使用上下文工具栏[插入链接](../email/message-tracking.md#insert-links)。

   ![](assets/opt-out-insert-link.png)

1. 从&#x200B;**[!UICONTROL 链接类型]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 外部选择退出/退订]**。

   ![](assets/opt-out-link-type.png)

1. 在&#x200B;**[!UICONTROL 链接]**&#x200B;字段中，将链接粘贴到您的第三方登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

### 为选择退出实施 API 调用 {#opt-out-api}

要在收件者從登陸頁面提交選擇時選擇退出，您必須實作 **訂閱API呼叫** 到 [Adobe Developer](https://developer.adobe.com){target="_blank"} 更新對應設定檔的偏好設定。

此 POST 调用如下：

端点：platform.adobe.io/journey/imp/consent/preferences

查询参数：

* **params**：包含加密后的有效负载
* **sig**：签名
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

[!DNL Journey Optimizer] 將透過以下方式使用這些引數更新對應設定檔的選擇 [Adobe Developer](https://developer.adobe.com){target="_blank"} API呼叫。

### 使用取消订阅链接发送消息 {#send-message-unsubscribe-link}

配置指向登陆页面的取消订阅链接并实施 API 调用后，即可发送消息。

1. 通过[历程](../building-journeys/journey.md)发送包含链接的消息。

1. 收到消息后，如果收件人单击取消订阅链接，则会显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人提交了表单（在此处，通过点击登陆页面中的 **Unsubscribe** 按钮），将通过 [API 调用](#opt-out-api)更新用户档案数据。

1. 然后，选择退出的收件人将被重定向至确认消息屏幕，提示收件人选择退出已成功完成。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次订阅，否则这个用户将不会收到来自您的品牌的通信。

1. 要检查相应用户档案的选择是否已更新，请转到 Experience Platform，并通过选择身份命名空间和相应的身份值访问该用户档案。進一步瞭解 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}.

   ![](assets/opt-out-profile-choice.png)

   在&#x200B;**[!UICONTROL 属性]**&#x200B;选项卡中，您可以看到&#x200B;**[!UICONTROL 选择]**&#x200B;的值已更改为&#x200B;**[!UICONTROL 否]**。

## 一键式选择退出 {#one-click-opt-out}

要在电子邮件中添加选择退出链接，请执行以下步骤。

1. [插入链接](../email/message-tracking.md#insert-links)并选择&#x200B;**[!UICONTROL 一键式选择退出]**&#x200B;作为链接类型。

   ![](assets/message-tracking-opt-out.png)

1. 输入用户取消订阅后将被重定向到的登陆页面的 URL。此页面仅用于确认选择退出是否成功。

   >[!NOTE]
   >
   >如果在渠道平面级别启用了 **List-Unsubscribe** 选项，则当用户单击电子邮件标头中的取消订阅链接时，也会使用此 URL。[了解详情](#unsubscribe-header)

   ![](assets/message-tracking-opt-out-confirmation.png)

   您可以个性化自己的链接。在[本节](../personalization/personalization-syntax.md)中了解更多关于个性化 URL 的信息。

1. 选择您要应用选择退出的层级：渠道、身份或订阅。

   ![](assets/message-tracking-opt-out-level.png)

   * **[!UICONTROL 渠道]**：选择退出适用于将来发送到当前渠道的用户档案目标（即电子邮件地址）的消息。如果多个目标与一个用户档案关联，则选择退出适用于该渠道的用户档案中的所有目标（即电子邮件地址）。
   * **[!UICONTROL 标识]**：选择退出适用于在将来发送给当前消息所使用的特定目标（即电子邮件地址）的消息。
   * **[!UICONTROL 订阅]**：选择退出适用于与特定订阅列表关联的将来发送的消息。仅在当前消息与订阅列表关联时，才能选择此选项。

1. 保存更改。

通过[历程](../building-journeys/journey.md)发送消息后，如果收件人点击了选择退出链接，会立即选择退出他们的用户档案。

## 电子邮件标头中的取消订阅链接 {#unsubscribe-header}

>[!CONTEXTUALHELP]
>id="ajo_admin_preset_unsubscribe"
>title="向电子邮件标头添加取消订阅链接"
>abstract="启用“列表取消订阅”以向电子邮件标头添加取消订阅链接。要设置取消订阅 URL，请在电子邮件内容中插入一个一键式选择退出链接。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html?lang=zh-Hans#one-click-opt-out" text="一键式选择退出"

如果在渠道平面级别启用 [List-Unsubscribe](../configuration/channel-surfaces.md#list-unsubscribe) 选项，使用 [!DNL Journey Optimizer] 发送的相应电子邮件将在电子邮件标头中包含取消订阅链接。

例如，取消订阅链接在 Gmail 中将会如下图这样显示：

![](assets/unsubscribe-header.png)

>[!NOTE]
>
>要在电子邮件标头中显示取消订阅链接，收件人的电子邮件客户端必须支持此功能。

取消订阅地址是相应渠道界面中显示的默认 **[!UICONTROL Mailto（取消订阅）]**&#x200B;地址。[了解详情](../configuration/channel-surfaces.md#list-unsubscribe)。

要设置个性化的取消订阅 URL，请在电子邮件内容中插入一键式选择退出链接，然后输入您选择的 URL。[了解详情](#one-click-opt-out)

根据电子邮件客户端的不同，单击标头中的取消订阅链接可能会产生以下影响：

* 取消订阅请求被发送到默认的取消订阅地址。

* 收件人被定向到您在向消息添加选择退出链接时指定的登陆页面 URL。

   >[!NOTE]
   >
   >如果您没有在消息内容中添加一键式选择退出链接，则不会显示登陆页面。

* 相应的用户档案会立即退出订阅，并且此选择将在 Experience Platform 中更新。進一步瞭解 [Experience Platform檔案](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}.
