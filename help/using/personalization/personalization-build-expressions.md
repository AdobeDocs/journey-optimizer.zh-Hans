---
solution: Journey Optimizer
product: journey optimizer
title: 添加个性化
description: 了解如何使用个性化编辑器添加个性化。
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
mini-toc-levels: 1
keywords: 表达式，编辑器，关于，开始
exl-id: 1ac2a376-a3a8-41ae-9b04-37886697f0fc
source-git-commit: 192542cf938c583093638c71a3d8728bbaf238b2
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 10%

---

# 添加个性化 {#build-personalization-expressions}

>[!CONTEXTUALHELP]
>id="ajo_perso_editor"
>title="关于个性化编辑器"
>abstract="个性化编辑器让您可以选择、排列、自定义和验证所有数据，为自己的内容创建定制的个性化。"

个性化编辑器是[!DNL Journey Optimizer]中个性化的核心。 它可在您需要定义个性化的每个上下文中使用，例如电子邮件、推送和选件。

在个性化编辑器界面中，您可以选择、排列、自定义和验证所有数据，为您的内容创建自定义个性化。

![](assets/perso_ee1.png)

## 可在何处添加个性化

您可以使用![添加个性化图标](assets/do-not-localize/add-perso-icon.svg)图标在每个字段中的&#x200B;**[!DNL Journey Optimizer]**&#x200B;中添加个性化。 展开以下部分，了解更多详细信息。

+++消息

在邮件中，可以在邮件的不同位置添加个性化，如&#x200B;**[!UICONTROL 主题行]**&#x200B;字段。

![](assets/perso_subject.png)

还可以在内容的其他部分中添加它。 例如，对于[推送通知](../push/push-gs.md)，可在&#x200B;**标题**、**正文**、**自定义声音**、**徽章**&#x200B;和&#x200B;**自定义数据**&#x200B;字段中添加个性化设置。

+++

+++向Designer发送电子邮件

在[电子邮件Designer](../email/get-started-email-design.md)中编辑电子邮件内容时，您可以使用上下文工具栏中的图标在文本块和URL中添加个性化设置。

![](assets/perso_insert.png)

+++

+++选件

在&#x200B;**优惠的表示形式**&#x200B;中使用文本类型内容时，您可以添加个性化。 [了解如何创建个性化优惠](../offers/offer-library/creating-personalized-offers.md)

+++

+++URLs

Journey Optimizer还允许您个性化消息中的&#x200B;**URL**。  个性化 URL 可将收件人引导至网站的特定页面，或引导至个性化的微型网站，具体取决于轮廓属性。URL个性化可用于以下类型的链接： **外部链接**、**退订链接**&#x200B;和&#x200B;**选择退出**。

个性化URL示例：

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

![](assets/perso-url.png){width="50%"}

>[!NOTE]
>
>在个性化编辑器中编辑个性化URL时，出于安全原因，将禁用帮助程序功能和受众成员资格。
>
>url内使用的个性化令牌不支持空格。

+++

+++电子邮件配置

创建电子邮件渠道配置时，您可以为子域、标题和URL跟踪参数定义个性化值。 [了解详情](../email/surface-personalization.md)

+++

## Personalization源 {#sources}

导航窗格允许您选择个性化的源。 可用源包括：

* **[!UICONTROL 配置文件属性]** ：列出与[Adobe Experience Platform数据模型(XDM)文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}中描述的配置文件架构关联的所有引用。
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
>abstract="切换该选项可让系统在您键入时自动建议并完成代码。此功能仅适用于 HTML 和文本格式，并支持轮廓和上下文属性。如果通过切换禁用，编辑器将提供原生 HTML 代码自动完成。"

中央工作区是您构建个性化语法的位置。 若要使用属性来个性化您的消息，请将其定位到左侧导航窗格中，然后单击`+`按钮以将其添加到表达式中。

![](assets/personalization-add-attribute.png)

`+`图标旁边的省略号菜单允许您获取每个属性的更多详细信息，并将最常用的属性添加到收藏夹。 添加到收藏夹的属性可从导航窗格中的&#x200B;**[!UICONTROL 收藏夹]**&#x200B;菜单访问。

>[!NOTE]
>
>默认情况下，属性窗格仅显示填充的属性。 要显示所有属性，请选择位于搜索字段上方的![](assets/do-not-localize/settings-icon.svg)按钮，然后关闭&#x200B;**[!UICONTROL 仅显示填充的属性]**&#x200B;选项。

此外，您可以定义在字符串类型配置文件属性为空时显示的默认回退文本。 为此，请单击属性旁边的省略号按钮，然后选择&#x200B;**[!UICONTROL 插入后备文本]**。 写入配置文件属性值为空时默认显示的文本，然后单击&#x200B;**[!UICONTROL 添加]**。

![](assets/attribute-details.png)

在以下示例中，个性化编辑器允许您选择今天生日的用户档案，然后插入对应于今天的特定选件以完成自定义。

![](assets/perso_ee2.png)

## 表达式编辑选项 {#options}

中央工作区提供了各种工具来帮助您编写个性化表达式。

![](assets/perso-workspace.png)

可用选项包括：

1. **[!UICONTROL 查找]** / **[!UICONTROL 查找并替换]**：搜索表达式并自动替换部分代码。
1. **[!UICONTROL 撤消]** / **[!UICONTROL 重做]**：撤消/重做上一个操作。
1. **[!UICONTROL 自动完成]**：在您键入时自动建议并完成代码。 此功能仅适用于 HTML 和文本格式，并支持轮廓和上下文属性。如果通过切换禁用，编辑器将提供原生 HTML 代码自动完成。

   ![](assets/perso-complete.png){width="70%" align="center" zoomable="yes"}

1. **[!UICONTROL HTML]** / **[!UICONTROL JSON]** / **[!UICONTROL 文本]**：标识代码格式。 这使系统能够根据所选语言调整验证和自动完成功能。
1. **[!UICONTROL 验证]**：检查表达式的语法。 有关详细信息，请参阅[此部分](../personalization/personalization-build-expressions.md)。
1. **[!UICONTROL 另存为片段]**：将表达式另存为表达式片段。 [在本节](../content-management/save-fragments.md#save-as-expression-fragment)中了解详情
1. **[!UICONTROL 字体大小]**：调整编辑器内内容的字体大小，以提高可读性。
1. **[!UICONTROL 自动换行]**：启用或禁用自动换行，从而允许在编辑器中单行显示或自动换行的长表达式。 选项包括：
   * **关**（默认） — 无自动换行。 长线延伸到编辑器视图之外，需要水平滚动。
   * **On** — 以编辑器的宽度换行。
   * **自动换行列** — 当行字符达到80个字符时换行。
   * **绑定** — 以编辑器宽度或80个字符（以较小者为准）换行。
1. **[!UICONTROL Picks]**：将属性显示为紧凑的“Picks”，通过隐藏长属性路径来提高可读性。 单击属性以显示其完整路径。

   >[!NOTE]
   >
   >药丸展示将在接下来的30天内逐步推广到所有环境。
   >
   >此选项仅适用于配置文件属性、上下文属性和Dynamic Media。

在导航窗格中，提供其他功能以帮助您构建个性化表达式。

![](assets/perso-features.png)

* **[!UICONTROL 辅助函数]** — 辅助函数允许您对数据执行操作，例如计算、数据格式或转换、条件，并在个性化上下文中处理这些操作。 [了解有关可用辅助函数的更多信息](functions/functions.md)

* **[!UICONTROL 收藏夹]** — 已添加到收藏夹的属性将显示在此列表中。 这允许您快速访问最常使用的项目。 若要向收藏夹添加属性，请单击省略号菜单，然后选择&#x200B;**[!UICONTROL 添加到收藏夹]**。

* **[!UICONTROL 条件]** — 利用在库中创建的条件规则将动态内容添加到消息中。 这允许您根据条件创建消息的多个变体。 [了解如何创建动态内容](../personalization/get-started-dynamic-content.md)

* **[!UICONTROL 片段]** — 利用已创建或已保存到当前沙盒的表达式片段。 片段是可重复使用的组件，可以在[!DNL Journey Optimizer]营销活动和历程中引用。 此功能允许预先构建多个自定义内容块，营销用户可以使用这些内容块在改进的设计过程中快速组合内容。 [了解如何使用表达式片段进行个性化](../personalization/use-expression-fragments.md)

在个性化表达式准备就绪后，需要由个性化编辑器验证该表达式。 有关详细信息，请参阅[此部分](../personalization/personalization-build-expressions.md)。

## 验证机制 {#validation-mechanisms}

单击&#x200B;**添加**&#x200B;按钮关闭编辑器窗口时，将自动执行表达式验证。 您还可以使用&#x200B;**验证**&#x200B;按钮检查个性化语法。

![](assets/perso_validation1.png)

展开以下部分可查看验证个性化设置时可能发生的常见错误。

+++常见错误

* **找不到“XYZ”路径**

尝试引用架构中未定义的字段时。

在这种情况下，**firstName1**&#x200B;未定义为配置文件架构中的特性：

```
{{profile.person.name.firstName1}}
```

* **变量“XYZ”的类型不匹配。 应为数组。 找到字符串。**

当尝试对字符串而不是数组进行迭代时。

在这种情况下，**product**&#x200B;不是数组：

```
{{each profile.person.name.firstName as |product|}}
 {{product.productName}}
{{/each}}
```

* **无效的Handlebars语法。 找到`'[XYZ}}'`**

当使用了无效的Handlebars语法时。

Handlebars表达式用&#x200B;**{{expression}}**&#x200B;括起来

```
   {{[profile.person.name.firstName}}
```

* **区段定义无效**

```
No segment definition found for 988afe9f0-d4ae-42c8-a0be-8d90e66e151
```

+++

对于选件，可能会发生特定错误。 有关更多详细信息，请展开以下部分：

+++ 与优惠相关的特定错误

与电子邮件或推送消息中的优惠集成相关的错误具有以下模式：

```
Offer.<offerType>.[PlacementID].[ActivityID].<offer-attribute>
```

验证是在验证个性化编辑器中的个性化内容期间执行的。

<table> 
 <thead> 
  <tr> 
   <th> 错误标题<br /> </th> 
   <th> 验证/解析<br /> </th> 
  </tr> 
 </thead> 
 <tbody> 
  <tr> 
   <td>未找到ID为placementID且类型为OfferPlacement的资源<br/>
未找到id为activityID且类型为OfferActivity的资源<br/></td> 
   <td>检查ActivityID和/或PlacementID是否可用</td> 
  </tr> 
   <tr> 
   <td>无法验证资源。</td> 
   <td>投放位置中的componentType应与offerType选件匹配</td> 
  </tr> 
   <tr> 
   <td>offerId中不存在公共URL。</td> 
   <td>图像选件（所有与决策和投放对关联的个性化和回退）应填充公共URL（deliveryURL不应为空）。</td> 
  </tr> 
  <tr> 
   <td>决策包含非配置文件属性。</td> 
   <td>选件模型用法应仅包含配置文件属性。</td> 
  </tr> 
  <tr> 
   <td>获取决策用法时出错。</td> 
   <td>当API尝试获取选件模型时，可能会发生此错误。</td> 
  </tr>
  <tr> 
   <td>选件属性offer-attribute无效。</td> 
   <td>检查选件drp中引用的选件属性是否有效。 以下是有效属性： <br/>
图像： deliveryURL， linkURL<br/>
文本： content<br/>
HTML：内容<br/></td> 
  </tr> 
 </tbody> 
</table>

+++
