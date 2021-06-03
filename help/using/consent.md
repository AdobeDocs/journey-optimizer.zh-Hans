---
title: 管理选择退出
description: 了解如何管理选择禁用和隐私
source-git-commit: 738d72e8f3ba204219086f19252220ff833369cb
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 1%

---

# 管理选择退出 {#consent}

![](assets/do-not-localize/badge.png)

使用[!DNL Journey Optimizer]跟踪收件人对通信的同意情况，并通过管理其偏好和订阅了解他们希望如何与您的品牌互动。<!--Their preferences and subscriptions are handled through Consent management.-->

GDPR等法规规定，您必须先遵守特定要求，然后才能使用数据主体提供的信息。 此外，数据主体应能够随时修改其同意。

**为什么这很重要？**

* 未能遵守这些法规会为您的品牌带来法律风险。
* 它有助于您避免向收件人发送未经请求的通信，这可能会使收件人将您的消息标记为垃圾邮件并损害您的声誉。

在[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=zh-Hans)中了解有关管理隐私和适用法规的更多信息。

<!--* Recipients should be able to opt-in/opt-out from receiving electronic communication through one or more channel
* Recipients expect the brand to offer preference centre capability that controls how brand should engage with them (example: channel of communication, invasive and non-invasive tracking etc). This helps to fulfil regulatory obligations and also facilitates quality engagement with recipient. 
* The third category is the capability to offer subscription to recipients (newsletter, etc)-->

## 选择退出管理{#opt-out-management}

法律规定，向收件人提供从品牌接收通信的取消订阅功能。 在[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/privacy/regulations/overview.html?lang=en#regulations)中了解有关适用法规的更多信息。

因此，在发送给收件人的每封电子邮件中，必须始终包含&#x200B;**取消订阅链接**:
* 单击此链接后，收件人将被定向到包含确认选择退出的按钮的登陆页面。
* 单击选择退出按钮后，将发起Adobe I/O调用，以使用此信息更新用户档案数据。 [了解有关此内容的更多信息](#consent-service-api)。

要添加取消订阅链接，请执行以下步骤：

1. 构建退订登陆页面。
1. 将登陆页面托管在您选择的第三方系统上。
1. [创建消](../../help/using/create-message.md) 息 [!DNL Journey Optimizer]。

   <!--The link to your landing page should contain a static URL and the profile ID.-->

1. 选择内容中的文本，然后使用上下文工具栏插入链接。

   ![](assets/opt-out-insert-link.png)

1. 从&#x200B;**[!UICONTROL Link type]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL Unsubscription link]**。

   ![](assets/opt-out-link-type.png)

1. 在&#x200B;**[!UICONTROL Unsubscription page URL]**&#x200B;帧中，将链接复制到登陆页面。

   ![](assets/opt-out-link-url.png)

1. 单击 **[!UICONTROL Save]**。

1. 保存内容并[发布消息](../../help/using/publish-manage-message.md)。

   >[!NOTE]
   >
   >您的第三方登陆页面URL将包含三个参数，用于通过Adobe I/O调用更新用户档案的首选项&#x200B;。 [在此部分中了解更多信息](#consent-service-api)。

1. 通过[journey](building-journeys/journey.md)发送包含登陆页面链接的消息。

1. 收到消息后，如果收件人单击取消订阅链接，则会显示您的登陆页面。

   ![](assets/opt-out-lp-example.png)

1. 如果收件人单击登陆页面中的选择退出按钮（此处为&#x200B;**取消订阅**&#x200B;按钮），则用户档案数据将通过[Adobe I/O调用](#opt-out-api)进行更新。

   然后，已选择退出的收件人将被重定向到确认消息屏幕，指示已成功退出。

   ![](assets/opt-out-confirmation-example.png)

   因此，该用户将不会收到来自您品牌的通信，除非再次订阅。

要检查相应配置文件的选择是否已更新，请转到Experience Platform，然后通过选择身份命名空间和相应的身份值来访问配置文件。 请参阅[Experience Platform文档](https://experienceleague.adobe.com/docs/experience-platform/profile/ui/user-guide.html?lang=en#getting-started)，以了解更多信息。

![](assets/opt-out-profile-choice.png)

在&#x200B;**[!UICONTROL Attributes]**&#x200B;选项卡中，您可以看到&#x200B;**[!UICONTROL choice]**&#x200B;的值已更改为&#x200B;**[!UICONTROL no]**。

<!--The opt-out URL is resolved upon each recipient receiving the message. It is then personalized with the relevant encrypted parameters (profile ID, profile name, journey ID, sandbox ID, and message execution ID).-->

## 选择退出API调用{#opt-out-api}

收件人通过单击取消订阅链接选择退出后，将调用Adobe I/OAPI <!--Consent service API to capture the encrypted data and-->以更新相应用户档案的首选项。

此Adobe I/OPOST调用如下所示：

端点：cjm.adobe.io/imp/consent/preferences

查询参数：
* **参数**:包含加密的有效负载
* **sig**:签名  <!--which signature?-->
* **pid**:加密的配置文件ID

这些参数可从发送给收件人的取消订阅链接中获取，即将为给定收件人打开第三方登陆页面的URL:

![](assets/opt-out-parameters.png)

<!--QUESTION: How do you get the URL built for each recipient? Do you have to wait until each targeted recipient receives the unsubscribe link or can you deduce it in advance? Is it done automatically upon the API call or do you have to do something manually for each profile? In other words will the LP automatically include the 3 parameters or do you have to insert something manually? Still not completely clear-->

标题要求：
* x-api-key
* x-gw-ims-org-id
* x-sandbox-name
* 授权（来自您技术帐户的用户令牌）<!--How do you find this information? And other header elements?-->

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

## 推送选择退出管理{#push-opt-out-management}

推送收件人可自行通过其设备取消订阅。

例如，下载或使用应用程序时，用户可以选择停止通知。 同样，他们也可以通过移动设备操作系统更改通知设置。
