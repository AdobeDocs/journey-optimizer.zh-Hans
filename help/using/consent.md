---
title: 管理选择退出机制
description: 了解如何管理选择退出机制和隐私
feature: 历程
topic: 内容管理
role: User
level: Intermediate
source-git-commit: a1ce789ad78f70bdb2a1387ffb6c60cb40b8b0bb
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 85%

---

# 管理选择退出机制 {#consent}

使用 [!DNL Journey Optimizer] 跟踪收件人对通信的许可，并通过管理其偏好和订阅了解他们希望如何与您的品牌互动。<!--Their preferences and subscriptions are handled through Consent management.-->

GDPR 等法规规定，您必须遵守特定要求才能使用数据主体的信息。此外，数据主体应当能够随时修改其许可。

**为什么这很重要？**

* 未能遵守这些法规会为您的品牌带来法律监管风险。
* 它有助于避免向收件人发送未经请求的通信，这种通信可能会使他们将您的消息标记为垃圾邮件并损害您的声誉。

在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)中进一步了解管理隐私和适用的法规。

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## 选择退出管理{#opt-out-management}

向收件人提供取消从品牌接收通信的功能是一项法律要求。在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=zh-Hans#regulations)中进一步了解适用的法规。

因此，您必须在发送给收件人的每封电子邮件中都加入&#x200B;**取消订阅链接**：
* 单击此链接后，收件人将被定向到一个包含确认取消订阅按钮的登陆页面。
* 点击选择退出按钮后，将进行 Adobe I/O 调用以使用此信息更新用户档案数据。[了解有关此内容的更多信息](#consent-service-api)。

要添加取消订阅链接，请执行以下步骤：

1. 构建退订登陆页面。
1. 在您选择的第三方系统上托管您的登陆页面。
1. 在 [!DNL Journey Optimizer] 上[创建消息](../../help/using/create-message.md)。

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. 在内容中选择文本，然后使用上下文工具栏插入链接。

   ![](assets/opt-out-insert-link.png)

1. 从 **[!UICONTROL Link type]** 下拉列表中选择 **[!UICONTROL Unsubscription link]**。

   ![](assets/opt-out-link-type.png)

1. 在 **[!UICONTROL Unsubscription page URL]** 框中，将链接复制到您的登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击 **[!UICONTROL Save]**。

1. 保存您的内容并[发布您的消息](../../help/using/publish-manage-message.md)。

   >[!NOTE]
   >
   >您的第三方登陆页面 URL 将包含三个参数，这些参数将用于通过 Adobe I/O 调用更新用户档案的偏好设置。[在本节中了解详情](#consent-service-api)。

1. 通过[历程](building-journeys/journey.md)将您的消息与指向登陆页面的链接一起发送。

1. 收到消息后，如果收件人单击取消订阅链接，将显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人单击登陆页面中的选择退出按钮（此处为&#x200B;**取消订阅**&#x200B;按钮），则会通过 [Adobe I/O 调用](#opt-out-api)更新用户档案数据。

   然后，选择退出的收件人将被重定向至确认消息屏幕，提示收件人选择退出已成功完成。

   ![](assets/opt-out-confirmation-example.png)

   因此，除非再次订阅，否则这个用户将不会收到来自您的品牌的通信。

要检查相应用户档案的选择是否已更新，请转到 Experience Platform，并通过选择身份命名空间和相应的身份值访问该用户档案。在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=zh-Hans#getting-started)中了解更多信息。

![](assets/opt-out-profile-choice.png)

在 **[!UICONTROL Attributes]** 选项卡中，您可以看到 **[!UICONTROL choice]** 的值已更改为 **[!UICONTROL no]**。

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## 选择退出时的 API 调用{#opt-out-api}

收件人通过单击取消订阅链接选择退出后，将调用 Adobe I/O API <!--Consent service API to capture the encrypted data and-->以更新相应用户档案的偏好设置。

这个 Adobe I/O POST 调用如下：

端点：cjm.adobe.io/imp/consent/preferences

查询参数：
* **params**：包含加密后的有效负载
* **sig**：签名 <!--which signature?-->
* **pid**：加密后的用户档案 ID

这些参数可以从发送到您的收件人的取消订阅链接中获取，即为特定收件人打开您的第三方登陆页面的 URL：

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

标头要求：
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授权（技术帐户中的用户令牌）<!--How do you find this information? And other header elements?-->

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

<!--The Consent service /-->[!DNL Journey Optimizer] will <!--decrypt and-->use these parameters to update the corresponding profile's choice. <!--and provide an answer back to the landing page.-->

## 标题{#unsubscribe-email}中的取消订阅链接

如果收件人的电子邮件客户端支持在电子邮件标题中显示取消订阅链接，则随[!DNL Journey Optimizer]一起发送的电子邮件会自动包含此链接。

例如，取消订阅链接在Gmail中将如下所示：

![](assets/unsubscribe-email.png)

根据电子邮件客户端的不同，单击标题中的取消订阅链接将产生以下影响之一：

* 相应的用户档案会立即退出，并且此选择将以Experience Platform更新。 在 [Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started)中了解更多信息。

* 它与单击电子邮件内容的取消订阅链接具有相同的效果：收件人将被重定向到包含确认选择退出的按钮的登陆页面。 在[此部分](#opt-out-management)中了解有关选择退出管理的更多信息。

## 推送退出管理{#push-opt-out-management}

推送收件人可以通过其设备取消订阅。

例如，在下载或使用应用程序时，用户可以选择停止发送通知。同样，他们可以通过移动操作系统更改通知设置。
