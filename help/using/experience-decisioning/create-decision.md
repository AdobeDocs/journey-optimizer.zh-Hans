---
title: 创建决策策略
description: 了解如何创建决策策略
feature: Decisioning
topic: Integrations
role: User
level: Experienced
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: ddb0a03461f37c7217486cc7fb8f28df83a90e59
workflow-type: tm+mt
source-wordcount: '1865'
ht-degree: 16%

---

# 创建决策策略 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="决策是什么？"
>abstract="决策策略包含决策引擎挑选最佳内容的所有选择逻辑。决策政策是针对特定活动的。他们的目标是为每个轮廓选择最佳的报价，而活动创作允许您指示如何呈现所选的决策项目，包括应在消息中包含哪些项目属性。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="关于决策"

>[!CONTEXTUALHELP]
>id="ajo_journey_decision_policy"
>title="定义决策策略"
>abstract="决策策略允许您从决策引擎中挑选最佳项目，并将其推送给合适的受众。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="关于决策"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_policy"
>title="决策策略"
>abstract="决策策略允许您从决策引擎中挑选最合适的项目并交付给每个受众。"

>[!CONTEXTUALHELP]
>id="ajo_exd_placements"
>title="投放"
>abstract="放置环境决定了决策引擎返回的项目在消息中出现的位置。您可以在报告中跟踪其在不同放置环境的性能。"

>[!CONTEXTUALHELP]
>id="ajo_exd_decision_attribute"
>title="从目录中选择决策属性"
>abstract="决策属性存储在目录的架构中。从所选目录中选择要在此使用的属性。"

决策策略是优惠的容器，它们利用决策引擎根据受众选择要投放的最佳内容。

<!--Decision policies contain all of the selection logic for the decisioning engine to pick the best content. Decision policies are campaign specific. -->其目标是为每个用户档案选择最佳优惠，而营销活动/历程创作允许您指示应如何显示选定的决策项目，包括要包含在消息中的项目属性。

>[!NOTE]
>
>在[!DNL Journey Optimizer]用户界面中，决策策略标记为决策<!--but they are decision policies. TBC if this note is needed-->。

将决策策略用于基于代码的营销活动的主要步骤如下：

1. [将决策策略添加到基于代码的体验](#add-decision)
1. [使用决策策略](#use-decision-policy)
1. [创建自定义Customer Journey Analytics报表仪表板](cja-reporting.md)

## 将决策策略添加到基于代码的体验 {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="定义要返回的项数"
>abstract="选择要返回的决策项数。例如，如果选择 2，则将为当前配置显示最佳的 2 个合格优惠。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="选择回退"
>abstract="在为该决策策略定义的所有选择策略均不合格时，向用户显示回退项。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="策略是什么？"
>abstract="选择策略的序列决定首先评估哪个策略。至少需要一个策略。将一同评估组合策略中的决策项。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/decisioning/offer-decisioning/get-started-decision/starting-offer-decisioning" text="创建策略"

要在您的网站或移动应用程序上向访客展示最佳的动态选件和体验，请将决策策略添加到基于代码的活动或历程。 要实现此目的，请执行以下步骤。

### 创建决策策略 {#add}

1. 创建营销活动并选择&#x200B;**[!UICONTROL 基于代码的体验]**&#x200B;操作。 [了解详情](../code-based/create-code-based.md)

1. 从[代码编辑器](../code-based/create-code-based.md#edit-code)中，选择&#x200B;**[!UICONTROL 决策策略]**，然后单击&#x200B;**[!UICONTROL 添加决策策略]**。

   ![](assets/decision-code-based-create.png)

   在历程或营销活动版本屏幕中，您还可以直接添加决策策略，而无需打开个性化编辑器。 使用右边栏上的专用图标显示&#x200B;**[!UICONTROL 决策]**&#x200B;部分。

   ![](../code-based/assets/code-based-campaign-show-decisioning.png)

1. 默认情况下，创建新策略。

   >[!NOTE]
   >
   >您还可以选择选择现有策略。

1. 填写决策策略的详细信息：添加名称并选择目录。

   >[!NOTE]
   >
   >当前只有默认的&#x200B;**[!UICONTROL 选件]**&#x200B;目录可用。

1. 选择要返回的项目数。 例如，如果选择2，则会为当前配置显示最佳的2个符合条件的优惠。 单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/decision-code-based-details.png)

### 选择项目和选择策略 {#select}

**[!UICONTROL 策略序列]**&#x200B;部分允许您选择要与决策策略一起呈现的决策项和选择策略。

1. 单击&#x200B;**[!UICONTROL 添加]**&#x200B;按钮。

1. 选择要包含在策略中的对象类型：

   * **[!UICONTROL 选择策略]**：添加一个或多个选择策略。 决策策略利用与资格约束和排名方法关联的集合来确定要显示的项目。 您可以选择现有的选择策略，也可以使用&#x200B;**[!UICONTROL 创建选择策略]**&#x200B;按钮创建新选择策略。 [了解如何创建选择策略](selection-strategies.md)

   * **[!UICONTROL 决策项]**：添加单个决策项以呈现，而无需通过选择策略运行。 一次只能选择一个决策项目。 将应用为物料设置的任何资格约束。

   ![](assets/decision-code-based-strategy-sequence.png)

   >[!NOTE]
   >
   >决策策略支持最多10个选择策略和决策项目组合。 [了解有关Decisioning护栏和限制的更多信息](gs-experience-decisioning.md#guardrails)

1. 添加多个决策项目和/或策略时，将按特定顺序评估它们。 将首先评估添加到序列中的第一个对象，依此类推。

   要更改默认顺序，您可以拖放对象和/或组以根据需要重新排序。 [了解详情](#evaluation-order)

### 在决策策略中管理评估顺序 {#evaluation-order}

将决策项和选择策略添加到策略中后，您可以安排它们的顺序以确定它们的评估顺序，并将选择策略组合在一起以一起评估它们。

每个对象或对象组左侧的数字表示用于计算项和策略的&#x200B;**顺序顺序**。 要在序列中移动选择策略（或一组策略）的位置，请将其拖放到另一个位置。

>[!NOTE]
>
>在序列中只能拖放选择策略。 要更改决策项的位置，您需要删除决策项，并在添加之前要评估的其他项后使用&#x200B;**[!UICONTROL 添加]**&#x200B;按钮重新添加它。

![](assets/decision-code-based-strategy-groups.png)

您还可以&#x200B;**将**&#x200B;多个选择策略组合到组中，以便一起评估而不是分别评估。 为此，请单击选择策略下的&#x200B;**`+`**&#x200B;按钮以将其与另一个策略组合。 您还可以将选择策略拖放到另一个策略上，以将这两个策略分组到一个组中。

>[!NOTE]
>
>决策项目不能与其他项目或选择策略一起分组。

多个策略及其分组决定了策略的优先级和合格优惠的排名。 第一种策略具有最高优先级，同一组内组合策略具有相同的优先级。

例如，您有两个集合，一个在策略A中，另一个在策略B中。该请求用于发送回两个决策项目。 假设策略A中有两个符合条件的优惠，而策略B中有三个符合条件的优惠。

* 如果两个策略不是&#x200B;**组合**&#x200B;或按顺序（1和2）组合，则第一个策略中的前两个符合条件的优惠将返回第一行。 如果第一个策略中没有两个符合条件的优惠，则决策引擎将依次转到下一个策略以查找仍然需要的任意数量的优惠，并且最终将在需要时返回回退。

  ![](assets/decision-code-based-consecutive-strategies.png)

* 如果同时&#x200B;**评估这两个集合**，则由于策略A中有两个符合条件的优惠和策略B中有三个符合条件的优惠，因此这五个优惠都将根据各自的排名方法确定的值栈叠在一起。 由于请求了两个选件，因此将返回这五个选件中符合条件的前两个选件。

  ![](assets/decision-code-based-combined-strategies.png)

+++ **具有多个策略的示例**

现在，我们来看一个示例，其中您将多个策略划分为不同的组。

你定义了三种策略。 策略1和策略2被归入组1，策略3独立（组2）。

每个策略的合格优惠及其优先级（用于排名功能评估）如下所示：

* 第1组：
   * 策略1 — （选件1、选件2、选件3） — 优先级1
   * 策略2 — （选件3、选件4、选件5） — 优先级1

* 第2组：
   * 策略3 — （选件5，选件6） — 优先级0

首先评估最高优先级的策略选件，并将其添加到排名选件列表。

**迭代1：**

将同时评估策略1和策略2选件（选件1、选件2、选件3、选件4、选件5）。 假设结果为：

选件1 - 10
选件2 - 20
战略1中的报价3 - 30，战略2中的报价45。 两者中的最高值将被考虑在内，因此会考虑45。
选件4 - 40
选件5 - 50

排名后的选件现在如下所示：选件5、选件3、选件4、选件2、选件1。

**迭代2：**

已评估策略3选件（选件5、选件6）。 假设结果为：

* 选件5 — 将不进行评估，因为上述结果中已存在该选件。
* 选件6 - 60

排名后的选件现在如下所示：选件5 、选件3、选件4、选件2、选件1、选件6。

+++

### 添加后备优惠 {#fallback}

选择决策项目和/或选择策略后，您可以添加备用优惠，如果上述项目或选择策略均不合格，则会向用户显示备用优惠。

![](assets/decision-code-based-strategy-fallback.png)

您可以从列表中选择任何项目，这将显示在当前沙盒中创建的所有决策项目。 如果没有符合条件的选择策略，则无论应用于所选项目<!--nor frequency capping when available - TO CLARIFY-->的日期和资格限制如何，都会向用户显示回退。

>[!NOTE]
>
>回退是可选的。 如果未选择任何回退，并且没有限定策略，则[!DNL Journey Optimizer]将不显示任何内容。 您可以合计决策策略所请求的项目数。 这样可确保在用例需要时返回特定数量的项目。

决策策略就绪后，保存该策略并单击&#x200B;**[!UICONTROL 创建]**。 现在，决策策略已创建，您可以在基于代码的体验内容中使用决策属性。 [了解详情](#use-decision-policy)

![](assets/decision-code-based-decision-added.png)

## 在代码编辑器中使用决策策略 {#use-decision-policy}

创建决策策略后，即可在[个性化编辑器](../code-based/create-code-based.md#edit-code)中使用。 要实现此目的，请执行以下步骤。

>[!NOTE]
>
>基于代码的体验利用[!DNL Journey Optimizer]个性化编辑器及其所有个性化和创作功能。 [了解详情](../personalization/personalization-build-expressions.md)

1. 单击&#x200B;**[!UICONTROL 插入策略]**&#x200B;按钮。 将添加与决策策略对应的代码。

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >此序列将按您希望返回决策策略的次数重复。 例如，如果您选择在[创建决策](#add-decision)时返回2个项目，则相同的序列将重复两次。

1. 现在，您可以在该代码中添加所需的所有决策属性。 可用的属性存储在&#x200B;**[!UICONTROL 优惠]**&#x200B;目录的架构中。 自定义属性存储在&#x200B;**`_<imsOrg`>**&#x200B;文件夹中，标准属性存储在&#x200B;**`_experience`**&#x200B;文件夹中。 [了解有关优惠目录架构的更多信息](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

   >[!NOTE]
   >
   >对于决策策略项目跟踪，决策策略内容需要按如下方式添加`trackingToken`属性：
   >`trackingToken: {{item._experience.decisioning.decisionitem.trackingToken}}`

1. 单击每个文件夹以将其展开。 将鼠标光标置于所需位置，然后单击要添加属性旁边的+图标。 您可以向代码添加任意数量的属性。

   ![](assets/decision-code-based-add-decision-attributes.png)

1. 确保将`#each`循环包裹在一对方括号`[ ]`内，并在结束`/each`前添加一个逗号。

   ![](assets/decision-code-based-wrap-code.png)

1. 您还可以添加个性化编辑器中可用的任何其他属性，例如配置文件属性。

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. 单击&#x200B;**[!UICONTROL 保存并关闭]**&#x200B;以确认更改。

1. 查看并发布基于代码的体验营销活动或历程。 [了解如何操作](../code-based/publish-code-based.md)

   现在，一旦您的开发人员进行API或SDK调用以获取渠道配置中定义的表面的内容，更改就会应用于您的网页或应用程序。

   >[!NOTE]
   >
   >目前，在使用决策的基于[代码的体验](../code-based/create-code-based.md)营销活动或历程中，您无法从用户界面模拟内容。 [此部分](../code-based/code-based-decisioning-implementations.md)中提供了解决方法。

1. 要查看决策的执行情况，您可以创建自定义[Customer Journey Analytics报告仪表板](cja-reporting.md)。


