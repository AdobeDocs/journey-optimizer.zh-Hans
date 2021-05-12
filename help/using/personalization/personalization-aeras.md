---
title: Journey Optimizer中的个性化上下文
description: 了解在哪些上下文中可以添加个性化
translation-type: tm+mt
source-git-commit: e73b47ab6243b13f82aa1503bd8c751f976f29ee
workflow-type: tm+mt
source-wordcount: '397'
ht-degree: 2%

---

# 个性化区域{#personalization-areas}

![](../assets/do-not-localize/badge.png)

Journey Optimizer传递的内容和消息显示可以通过多种不同的方式进行个性化。

与编辑器图标关联的所有字段均可打开个性化编辑器并接收个性化内容。

![](assets/perso_icon.png)

## 个性化您的电子邮件

在创建电子邮件渠道消息时，**电子邮件主题**&#x200B;字段可个性化。

![](assets/perso_subject.png)

在电子邮件设计器中，您可以个性化内容：

* 在&#x200B;**消息**&#x200B;中：在文本块内单击，单击上下文工具栏中的&#x200B;**个性化**&#x200B;图标，然后选择&#x200B;**插入个性化**&#x200B;字段。 有关“电子邮件设计器”界面的详细信息，请参阅此[部分](../design-emails.md)。

   ![](assets/perso_insert.png)

* 对于&#x200B;**链接**:选择文本块中的某些文本或图像，单击上下文工具栏中的&#x200B;**插入链接**&#x200B;图标。 在窗口中，您可以单击&#x200B;**添加个性化**&#x200B;图标来添加个性化区块。

   ![](assets/perso_link.png)

## 个性化推送通知

在&#x200B;**推送渠道**&#x200B;中，个性化允许您微调推送通知。

您可以在以下字段中添加个性化：

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

有关推送通知配置的完整文档，请参阅[本节](../configure-push.md)。


## 使用表达式编辑器

表达式编辑是Journey Optimizer中个性化的核心。

它适用于您需要定义个性化(如电子邮件、推送和优惠)的所有环境。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以便为您的内容创建自定义的个性化。

![](assets/perso_ee1.png)

屏幕的左侧部分显示一个域选择器，通过它可以选择个性化的源。

* **用户档案** :列表与用户档案模式(XDM)文档中描述 [的Adobe Experience Platform相关的所有引用](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。
* **细分会员资格** :列表在Adobe Experience Platform分段服务中创建的所有区段。有关分段的详细信息[此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)。
* **优惠** :列表与特定位置关联的所有优惠。选择位置，然后在内容中插入优惠。 有关如何管理优惠的完整文档，请参阅[本节](../../using/offers/get-started/starting-offer-decisioning.md)。

选择后，该引用将添加到编辑器中。

>[!NOTE]
>
>“+”图标旁边的“信息”图标将打开一个工具提示，其中提供了每个变量的更多详细信息。

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后通过插入与当天对应的特定优惠来完成自定义。

![](assets/perso_ee2.png)




