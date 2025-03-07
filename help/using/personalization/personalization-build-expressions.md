---
solution: Journey Optimizer
product: journey optimizer
title: 关于个性化编辑器
description: 了解如何使用个性化编辑器。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器，关于，开始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 155ae8ef14e5482d94e54b15962afa09aa6826fc
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 16%

---

# 开始使用个性化编辑器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于个性化编辑器"
>abstract="个性化编辑器让您可以选择、排列、自定义和验证所有数据，为自己的内容创建定制的个性化。"

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="自动完成"
>abstract="切换该选项可让系统在您输入表达式时自动完成代码并提出建议。此选项仅适用于 HTML 和文本格式。"

个性化编辑器是[!DNL Journey Optimizer]中个性化的核心。 它可在您需要定义个性化的每个上下文中使用，例如电子邮件、推送和选件。

在个性化编辑器界面中，您将选择、排列、自定义和验证所有数据，以创建内容的自定义个性化设置。

![](assets/perso_ee1.png)

## 可用的个性化源 {#sources}

屏幕左侧显示一个域选择器，允许您选择个性化的源。 可用源包括：

* **[!UICONTROL 配置文件属性]** ：列出与[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}中描述的配置文件架构关联的所有引用。
* **[!UICONTROL 受众]** ：列出在Adobe Experience Platform分段服务中创建的所有受众。 有关分段的更多信息，请参阅[此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}。
* **[!UICONTROL 优惠决策]** ：列出与特定投放位置关联的所有优惠。 选择投放位置，然后在您的内容中插入选件。 有关如何管理优惠的完整文档，请参阅[此部分](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 上下文属性]** ：在历程或营销活动中使用渠道操作活动（电子邮件、推送、短信）时，与事件和属性相关的上下文属性可用于个性化。 [此部分](personalization-use-case.md)中介绍了利用上下文属性的个性化示例。
* **[!UICONTROL 辅助函数]** ：列出所有可用于对数据执行操作（如计算、数据格式或转换、条件）的辅助函数，并在个性化上下文中处理这些函数。 有关详细信息，请参阅[此部分](functions/functions.md)。

## 添加个性化属性 {#add}

单击+按钮可向个性化表达式添加属性。

通过“+”图标旁边的省略号菜单，可获取每个变量的更多详细信息并将最常用的属性添加到收藏夹。 [了解如何将属性添加到收藏夹](personalization-favorites.md)

>[!NOTE]
>
>如果您使用使用合成工作流生成的扩充属性定位受众，则可以利用这些扩充属性个性化您的消息。 [了解如何使用受众扩充属性](../audience/about-audiences.md#enrichment)

此外，您可以定义在字符串类型配置文件属性为空时显示的默认回退文本。 为此，请单击属性旁边的省略号按钮，然后选择&#x200B;**[!UICONTROL 插入后备文本]**。 写入配置文件属性值为空时默认显示的文本，然后单击&#x200B;**[!UICONTROL 添加]**。

![](assets/attribute-details.png)

在以下示例中，个性化编辑器允许您选择今天生日的用户档案，然后插入对应于今天的特定选件以完成自定义。

![](assets/perso_ee2.png)

在个性化表达式准备就绪后，需要由个性化编辑器验证该表达式。 有关详细信息，请参阅[此部分](personalization-validation.md)。
