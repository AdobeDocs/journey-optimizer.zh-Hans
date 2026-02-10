---
title: 在消息中使用决策策略
description: 了解如何在消息中使用决策策略。
feature: Decisioning
topic: Integrations
role: User
level: Experienced
mini-toc-levels: 1
version: Journey Orchestration
exl-id: 35fc3cf2-1b91-4f30-ad71-f9d7d2a0291c
source-git-commit: 71a5b2163500b26ef3ea61e55d18cad539bfeb7f
workflow-type: tm+mt
source-wordcount: '723'
ht-degree: 3%

---

# 在消息中使用决策策略 {#create-decision}

将决策策略添加到内容后，您可以使用返回决策项中的属性进行个性化。 为此，请先在内容中插入决策策略代码。

>[!CAUTION]
>
>决策策略适用于&#x200B;**基于代码的体验**、**短信**&#x200B;和&#x200B;**推送通知**&#x200B;渠道的所有客户。
>
>针对&#x200B;**电子邮件**&#x200B;渠道的决策仅在有限可用性中可用。 要请求获取访问权限，请联系您的Adobe代表。 了解有关[可用性标签](../rn/releases.md#availability-labels)的更多信息。

## 插入决策策略代码 {#insert}

>[!BEGINTABS]

>[!TAB 基于代码的体验]

1. 编辑您的基于代码的体验，并导航到&#x200B;**[!UICONTROL 决策策略]**。

2. 选择&#x200B;**[!UICONTROL 插入策略]**&#x200B;以添加决策策略代码。

   ![](assets/decision-code-based-add-decision.png)

>[!NOTE]
>
>对于基于代码的体验，如果您的决策策略包含决策项（包括片段），则可以在决策策略代码中利用这些片段。 [了解如何利用片段](fragments-decision-policies.md)

>[!TAB 电子邮件]

1. 打开&#x200B;**Personalization编辑器**&#x200B;并导航到&#x200B;**[!UICONTROL 决策策略]**。

2. 选择&#x200B;**[!UICONTROL 插入语法]**&#x200B;以添加决策策略的代码。

   ![](assets/decision-policy-add.png)

   >[!NOTE]
   >
   >如果未显示插入选项，则可能已为父组件配置了决策策略。

3. 如果尚未为组件分配位置，请从列表中选择一个位置，然后单击&#x200B;**[!UICONTROL 分配]**。

   ![](assets/decision-policy-placement.png)

>[!TAB 短信]

1. 打开&#x200B;**Personalization编辑器**&#x200B;并导航到&#x200B;**[!UICONTROL 决策策略]**。

2. 选择&#x200B;**[!UICONTROL 插入语法]**&#x200B;以添加决策策略的代码。

   ![](assets/decision-policy-add-sms-insert-syntax.png)

>[!TAB 推送]

1. 打开&#x200B;**Personalization编辑器**&#x200B;并导航到&#x200B;**[!UICONTROL 决策策略]**。

2. 选择&#x200B;**[!UICONTROL 插入语法]**&#x200B;以添加决策策略的代码。

   ![](assets/decision-policy-add-push-insert-syntax.png)

>[!IMPORTANT]
>
>包含推送通知的Experience Decisioning需要特定版本的Mobile SDK。 在实施此功能之前，请查看[发行说明](https://developer.adobe.com/client-sdks/home/release-notes/){target="_blank"}以确定所需的版本，并确保您已相应地升级。 您还可以在[此部分](https://developer.adobe.com/client-sdks/home/current-sdk-versions/){target="_blank"}中查看您的平台的所有可用SDK版本。

>[!ENDTABS]

将添加决策策略代码。 您现在可以使用返回决策项中的属性来个性化您的内容。

>[!NOTE]
>
>对于基于代码的体验和电子邮件渠道，请为每个要返回的决策项目重复此序列一次。 例如，如果您选择在[创建决策](create-decision-policy.md)时返回2个项目，请重复该序列两次。 对于短信和推送渠道，只能返回一个决策项。

## 使用决策项目属性进行个性化 {#attributes}

在内容中添加决策策略的代码后，返回决策项中的所有属性都可用于个性化。 [了解如何使用个性化](../personalization/personalize.md)。

属性存储在“选件”[目录架构](catalogs.md)中。 它们显示在个性化编辑器的以下文件夹中：
* **自定义属性**： `_\<imsOrg\>`文件夹
* **标准属性**： `_experience`文件夹

默认情况下，[!DNL Journey Optimizer]片段不支持决策项属性和上下文属性。 但是，您可以改用全局变量，如下所述。

![](assets/decision-code-based-decision-attributes.png)

要添加属性，请单击该属性旁边的&#x200B;**`+`**&#x200B;图标。 您可以根据需要添加任意数量的属性。 您还可以包括其他个性化属性，例如配置文件数据。

* 对于&#x200B;**电子邮件**&#x200B;和&#x200B;**基于代码的**&#x200B;渠道，使用方括号`#each`将`[ ]`循环中的属性换行，并在结束`/each`标记之前添加逗号。

  +++查看示例

  ![](assets/decision-code-based-wrap-code.png)

  +++

* 对于&#x200B;**短信**&#x200B;和&#x200B;**推送**&#x200B;渠道，请确保在决策策略的语法代码后插入属性。 此语法应始终保留在第1行。

  +++查看示例

  ![](assets/decision-added-sms.png)

  +++

  >[!NOTE]
  >如果在SMS或推送内容中插入图像资产属性（例如，在标题或正文中），则属性值将显示为URL。 图像本身不会呈现在这些字段中。

* 要启用决策项跟踪，请添加`trackingToken`属性： `trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

## 预览和测试内容

构建内容后，在激活历程或营销活动之前预览和测试内容。 决策项目根据模拟界面中选择的用户档案呈现。 [了解如何预览和测试内容](../content-management/preview-test.md)。

## 后续步骤 {#final-steps}

内容准备就绪后，查看并发布活动或历程：

* [发布历程](../building-journeys/publish-journey.md)
* [查看和激活营销活动](../campaigns/review-activate-campaign.md)

对于基于代码的体验，只要开发人员进行API或SDK调用以获取渠道配置中定义的界面的内容，所做的更改就会应用于您的网页或应用程序。

>[!NOTE]
>
>您当前无法为[基于代码的体验](../code-based/create-code-based.md)营销活动或历程模拟基于决策的内容。 [此处](../code-based/code-based-decisioning-implementations.md)提供了解决方法。

## 使用报告仪表板

要查看决策的执行情况，您可在营销活动或历程报告中查看现成的决策指标，或构建自定义Customer Journey Analytics功能板以测量绩效并深入了解决策政策和优惠的交付方式和参与方式。 [了解有关Decisioning报告的更多信息](cja-reporting.md)。

![](../reports/assets/cja-decisioning-item-performance.png)
