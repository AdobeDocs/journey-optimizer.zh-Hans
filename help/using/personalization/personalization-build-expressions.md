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
source-git-commit: ff6619925a36d2687922d1b631d1cabbcb98167e
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 6%

---

# 开始使用个性化编辑器 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于个性化编辑器"
>abstract="个性化编辑器让您可以选择、排列、自定义和验证所有数据，为自己的内容创建定制的个性化。"

个性化编辑器是[!DNL Journey Optimizer]中个性化的核心。 它可在您需要定义个性化的每个上下文中使用，例如电子邮件、推送和选件。

在个性化编辑器界面中，您将选择、排列、自定义和验证所有数据，以创建内容的自定义个性化设置。

![](assets/perso_ee1.png)

## Personalization源 {#sources}

屏幕左侧显示一个域选择器，允许您选择个性化的源。 可用源包括：

* **[!UICONTROL 配置文件属性]** ：列出与[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target="_blank"}中描述的配置文件架构关联的所有引用。
* **[!UICONTROL 受众]** ：列出在Adobe Experience Platform分段服务中创建的所有受众。 有关分段的更多信息，请参阅[此处](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=zh-Hans){target="_blank"}。
* **[!UICONTROL 优惠决策]** ：列出与特定投放位置关联的所有优惠。 选择投放位置，然后在您的内容中插入选件。 有关如何管理优惠的完整文档，请参阅[此部分](../offers/get-started/starting-offer-decisioning.md)。
* **[!UICONTROL 上下文属性]** ：在历程或营销活动中使用渠道操作活动（电子邮件、推送、短信）时，与事件和属性相关的上下文属性可用于个性化。 [此部分](personalization-use-case.md)中介绍了利用上下文属性的个性化示例。

>[!NOTE]
>
>如果您使用使用合成工作流生成的扩充属性定位受众，则可以利用这些扩充属性个性化您的消息。 [了解如何使用受众扩充属性](../audience/about-audiences.md#enrichment)

## 添加个性化 {#add}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor_autocomplete"
>title="自动完成"
>abstract="切换此选项可让系统在您键入时自动建议并完成代码。 此功能仅适用于HTML和文本格式，并且支持配置文件和上下文属性。 如果通过切换禁用，则编辑器将提供本机HTML代码自动完成。"

中央工作区是您构建个性化语法的位置。 若要使用属性来个性化您的消息，请将其定位到左侧导航窗格中，然后单击`+`按钮以将其添加到表达式中。

`+`图标旁边的省略号菜单允许您获取每个属性的更多详细信息，并将最常用的属性添加到收藏夹。 添加到收藏夹的属性可从左侧导航窗格中的&#x200B;**[!UICONTROL 收藏夹]**&#x200B;菜单访问。

此外，您可以定义在字符串类型配置文件属性为空时显示的默认回退文本。 为此，请单击属性旁边的省略号按钮，然后选择&#x200B;**[!UICONTROL 插入后备文本]**。 写入配置文件属性值为空时默认显示的文本，然后单击&#x200B;**[!UICONTROL 添加]**。

![](assets/attribute-details.png)

在以下示例中，个性化编辑器允许您选择今天生日的用户档案，然后插入对应于今天的特定选件以完成自定义。

![](assets/perso_ee2.png)

## 表达式编辑工具

中央工作区提供了各种工具来帮助您编写个性化表达式。

![](assets/perso-workspace.png)

可用选项包括：

1. **[!UICONTROL 查找]** / **[!UICONTROL 查找并替换]**：搜索表达式并自动替换部分代码。
1. **[!UICONTROL 撤消]** / **[!UICONTROL 重做]**：撤消/重做上一个操作。
1. **[!UICONTROL 自动完成]**：在您键入时自动建议并完成代码。 此功能仅适用于HTML和文本格式，并且支持配置文件和上下文属性。 如果通过切换禁用，则编辑器将提供本机HTML代码自动完成。

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL 文本]**：标识代码格式。 这使系统能够根据所选语言调整验证和自动完成功能。
1. **[!UICONTROL 验证]**：检查表达式的语法。 有关详细信息，请参阅[此部分](personalization-validation.md)。
1. **[!UICONTROL 另存为片段]**：将表达式另存为表达式片段。 [在本节](../content-management/save-fragments.md#save-as-expression-fragment)中了解详情
1. **[!UICONTROL 字体大小]**：调整编辑器内内容的字体大小，以提高可读性。
1. **[!UICONTROL 自动换行]**：启用或禁用自动换行，从而允许在编辑器中单行显示或自动换行的长表达式。 选项包括：
   * **关**（默认） — 无自动换行。 长线延伸到编辑器视图之外，需要水平滚动。
   * **On** — 以编辑器的宽度换行。
   * **自动换行列** — 当行字符达到80个字符时换行。
   * **绑定** — 以编辑器宽度或80个字符（以较小者为准）换行。

在导航窗格中，提供其他功能以帮助您构建个性化表达式。

![](assets/perso-features.png)

* **[!UICONTROL 辅助函数]** — 辅助函数允许您对数据执行操作，例如计算、数据格式或转换、条件，并在个性化上下文中处理这些操作。 [了解有关可用辅助函数的更多信息](functions/functions.md)

* **[!UICONTROL 收藏夹]** — 已添加到收藏夹的属性将显示在此列表中。 这允许您快速访问最常使用的项目。 若要向收藏夹添加属性，请单击省略号菜单，然后选择&#x200B;**[!UICONTROL 添加到收藏夹]**。

* **[!UICONTROL 条件]** — 利用在库中创建的条件规则将动态内容添加到消息中。 这允许您根据条件创建消息的多个变体。 [了解如何创建动态内容](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL 片段]** — 利用已创建或已保存到当前沙盒的表达式片段。 片段是可重复使用的组件，可以在[!DNL Journey Optimizer]营销活动和历程中引用。 此功能允许预先构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合内容。 [了解如何使用表达式片段进行个性化](../personalization/use-expression-fragments.md)

在个性化表达式准备就绪后，需要由个性化编辑器验证该表达式。 有关详细信息，请参阅[此部分](personalization-validation.md)。
