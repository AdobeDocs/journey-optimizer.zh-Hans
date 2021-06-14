---
title: Journey Optimizer中的个性化上下文
description: 了解在哪些上下文中可以添加个性化
feature: 个性化
topic: 个性化
role: Data Engineer
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%

---

# 个性化上下文和工具{#personalization-areas}

![](../assets/do-not-localize/badge.png)

Journey Optimizer投放的消息的内容和显示可以通过几种不同的方式进行个性化。

与编辑器图标关联的所有字段都可以打开个性化编辑器并接收个性化内容。

![](assets/perso_icon.png)

## 个性化电子邮件

创建电子邮件时，可以在邮件的&#x200B;**Email subject**&#x200B;字段中添加个性化。

![](assets/perso_subject.png)

在电子邮件设计器中，您可以个性化内容：

* 在&#x200B;**message**&#x200B;中：在文本块内单击，单击上下文工具栏中的&#x200B;**Personalize**&#x200B;图标，然后选择&#x200B;**插入个性化**&#x200B;字段。 有关Email Designer界面的更多信息，请参阅此[部分](../design-emails.md)。

   ![](assets/perso_insert.png)

* 对于&#x200B;**链接**:选择文本块中的某些文本或图像，单击上下文工具栏中的&#x200B;**插入链接**&#x200B;图标。 在窗口中，您可以通过单击&#x200B;**添加个性化**&#x200B;图标来添加个性化块。

   ![](assets/perso_link.png)

## 个性化推送通知

您还可以在以下字段中个性化您的&#x200B;**推送通知**:

* **标题**
* **正文**
* **自定义声音**
* **徽章**
* **自定义数据**

![](assets/perso_push.png)

详细了解[此部分](../create-push.md)中的推送通知配置。

## 使用表达式编辑器

表达式编辑器是Journey Optimizer中个性化的核心内容。

它在您需要定义个性化（如电子邮件、推送和选件）的每个上下文中均可用。

在表达式编辑器界面中，您将选择、排列、自定义和验证所有数据，以为您的内容创建自定义个性化。

![](assets/perso_ee1.png)

屏幕的左侧部分显示一个域选择器，用于选择个性化的源。

* **用户档案** :列出与Adobe Experience Platform数据模型(XDM)文档中所述的配 [置文件架构关联的所有引用](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans)。
* **区段成员资格** :列出在Adobe Experience Platform分段服务中创建的所有区段。有关可用分段的更多信息（[此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=en)）
* **选件** :列出与特定版面关联的所有选件。选择版面，然后在内容中插入选件。 有关如何管理选件的完整文档，请参阅[此部分](../deliver-personalized-offers.md)
* **上下文** :在历程 **** 中使用消息活动时，此菜单中提供了上下文历程字段。请参阅[此部分](personalization-use-case.md)
* **帮助程序函数** :列出可用于对数据执行操作的所有帮助程序函数，例如计算、数据格式或转化、条件，并在个性化环境中处理这些函数。[了解详情](functions/functions.md)



选择后，将在编辑器中添加引用。

>[!NOTE]
>
>“+”图标旁边的信息图标将打开工具提示，其中提供了每个变量的更多详细信息。

在以下示例中，表达式编辑器允许您选择今天生日的用户档案，然后通过插入与当天对应的特定选件来完成自定义。

![](assets/perso_ee2.png)




