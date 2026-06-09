---
solution: Journey Optimizer
product: journey optimizer
title: 编辑API触发的营销活动内容
description: 了解如何编辑API触发的活动内容。
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: 营销活动， API触发， REST，优化器，消息
exl-id: b7f12c65-c1af-4c49-b126-c13a51940a43
TQID: https://experienceleague.adobe.com/bGwpeOAxkX8JWh2c-CNrq7-L1YphGT0aoQvUJBia4IE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 450
ht-degree: 2%

---

# 编辑API触发的营销活动内容 {#api-content}

要配置消息内容，请导航到&#x200B;**[!UICONTROL 内容]**&#x200B;选项卡或单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮。

![](assets/campaign-content.png)

## 设计内容 {#design}

内容创建过程取决于您选择的渠道。 在以下页面中了解创建消息内容的详细步骤：

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../email/create-email.md"><img alt="电子邮件" src="../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../email/create-email.md"><strong>电子邮件</strong></a></div></td>
<td><a href="../mobile/create-mobile-message.md"><img alt="短信" src="../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../mobile/create-mobile-message.md"><strong>短信</strong></a></div></td>
<td><a href="../push/create-push.md"><img alt="推送" src="../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../push/create-push.md"><strong>推送通知</strong></a></div></td>
</tr></table>

>[!IMPORTANT]
>
>[高吞吐量营销活动](../campaigns/api-triggered-high-throughput.md)不依赖于Adobe配置文件：所有个性化必须作为上下文数据包含在API有效负载中，如下所述。 此模式仅适用于美国地区的电子邮件渠道。

## 使用上下文数据个性化内容 {#contextual}

您可以将其他数据传递到API有效负荷，以利用这些数据将消息个性化。

让我们举一个例子，客户希望重置密码，而您希望向他们发送一个在第三方工具中生成的密码重置URL。 借助API触发的营销活动，您可以将此生成的URL传递到API有效负荷中，并将其用于营销活动以将其添加到消息中。

为此，您需要将它们传递到API有效负荷，并使用个性化编辑器将它们添加到消息中。 使用`{{context.<contextualAttribute>}}`语法，其中`<contextualAttribute>`应与包含要传递的数据的API有效负载中的变量名称匹配。

请注意，目前没有上下文属性可用于左边栏菜单。 属性必须直接在个性化表达式中键入，[!DNL Journey Optimizer]不执行任何检查。

![](assets/api-triggered-context.png)

**必须读取**

* 传递到请求的上下文属性不能超过200kb，并且始终被视为字符串类型。
* `context.system`语法限制为仅供Adobe内部使用，不应用于传递上下文属性。
* 与启用配置文件的事件不同，在REST API中传递的上下文数据用于一次性通信，而不是针对配置文件进行存储。 创建的配置文件最多包含命名空间详细信息（如果发现缺少该配置文件）。
* 在内容中使用大量或繁重的上下文数据可能会影响性能。

## 测试和检查您的内容

定义内容后，使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮预览和测试内容。 您可以使用以下任一模拟方法：

* 单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;以测试内容变体与样本输入数据或AI自动生成。
* 单击&#x200B;**[!UICONTROL 模拟内容]**，然后从下拉列表中选择&#x200B;**[!UICONTROL 模拟内容（AEP配置文件）]**&#x200B;以使用测试配置文件进行预览。

[了解如何预览和测试内容](../content-management/preview-test.md)。 要浏览回促销活动创建屏幕，请单击向左箭头。

![](assets/create-campaign-design.png)

## 后续步骤 {#next}

准备好营销活动配置和内容后，即可定义营销活动受众。 [了解详情](api-triggered-campaign-audience.md)
