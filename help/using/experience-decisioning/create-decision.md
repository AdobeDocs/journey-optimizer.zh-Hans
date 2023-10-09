---
title: 创建决策
description: 了解如何创建决策
feature: Offers
topic: Integrations
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Beta 版"
exl-id: 63aa1763-2220-4726-a45d-3a3a8b8a55ec
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '1242'
ht-degree: 19%

---

# 创建决策策略 {#create-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_decision"
>title="决策是什么？"
>abstract="决策策略利用体验决策引擎根据受众选取最适合投放的内容。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html" text="关于体验决策"

>[!BEGINSHADEBOX]

本文档指南包括以下内容：

* [开始使用 Experience Decisioning](gs-experience-decisioning.md)
* 管理您的决策项目
   * [配置项目目录](catalogs.md)
   * [创建决策项目](items.md)
   * [管理项目集合](collections.md)
* 配置项目的选择
   * [创建决策规则](rules.md)
   * [创建排名方法](ranking.md)
* [创建选择策略](selection-strategies.md)
* **[创建决策策略](create-decision.md)**

>[!ENDSHADEBOX]

决策策略是优惠的容器，它们利用Experience Decisioning引擎根据受众选择要投放的最佳内容。

>[!NOTE]
>
>在 [!DNL Journey Optimizer] 用户界面中，决策策略标记为决策<!--but they are decision policies. TBC if this note is needed-->.

## 向基于代码的营销活动添加决策策略 {#add-decision}

>[!CONTEXTUALHELP]
>id="ajo_code_based_item_number"
>title="定义要返回的项数"
>abstract="选择要返回的决策项数。例如，如果选择 2，则将为当前表面显示最佳的 2 个合格优惠。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_fallback"
>title="选择回退"
>abstract="在为该决策策略定义的所有选择策略均不合格时，向用户显示回退项。"

>[!CONTEXTUALHELP]
>id="ajo_code_based_strategy"
>title="策略是什么？"
>abstract="选择策略的顺序决定首先评估哪个策略。至少需要一个策略。将一同评估组合策略中的决策项。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html" text="创建策略"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/offer-decisioning/get-started-decision/starting-offer-decisioning.html" text="评估顺序"

要在您的网站或移动应用程序上向访客展示最佳的动态选件和体验，请向基于代码的营销活动添加决策策略。 要实现此目的，请执行以下步骤。

1. 创建营销策划并选择 **[!UICONTROL 代码库体验(Beta)]** 操作。 [了解详情](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >基于代码的体验功能目前作为测试版提供，仅限部分用户使用。

1. 从 [代码编辑器](../code-based/create-code-based.md#edit-code)，选择 **[!UICONTROL 决策]** 图标并单击 **[!UICONTROL 创建决策]**.

   ![](assets/decision-code-based-create.png)

1. 填写决策策略的详细信息：添加名称并选择目录。

   >[!NOTE]
   >
   >当前仅默认 **[!UICONTROL 选件]** 目录可用。

   ![](assets/decision-code-based-details.png)

1. 选择要返回的项目数。 例如，如果选择 2，则将为当前表面显示最佳的 2 个合格优惠。单击 **[!UICONTROL 下一个]**

1. 使用 **[!UICONTROL 添加策略]** 按钮定义决策策略的选择策略。 每个策略包括与资格限制关联的优惠收藏集以及确定要显示的优惠的排名方法。 [了解详情](selection-strategies.md)

   ![](assets/decision-code-based-strategies.png)

   >[!NOTE]
   >
   >至少需要一个策略。不能添加超过10个策略。

1. 从 **[!UICONTROL 添加策略]** 屏幕，您还可以创建策略。 此 **[!UICONTROL 创建选择策略]** 按钮会将您重定向到 **[!UICONTROL Experience decisioning]** > **[!UICONTROL 配置]** 菜单。 [了解详情](selection-strategies.md)

   ![](assets/decision-code-based-add-strategy.png)

1. 添加多个策略时，将按特定顺序评估它们。 将首先评估添加到序列中的第一个策略，以此类推。 [了解详情](#evaluation-order)

   要更改默认顺序，您可以拖放策略和/或组以根据需要重新排序。

   ![](assets/decision-code-based-strategy-groups.png)

1. 添加后备。 如果上述选择策略均不合格，则会向用户显示回退项目。

   ![](assets/decision-code-based-strategy-fallback.png)

   您可以从列表中选择任何项目，这将显示在当前沙盒中创建的所有决策项目。 如果没有符合条件的选择策略，则无论应用于选定项目的日期和资格限制如何，都会向用户显示回退<!--nor frequency capping when available - TO CLARIFY-->.

   >[!NOTE]
   >
   >回退是可选的。 如果未选择任何回退，并且没有限定策略，则不会显示任何内容。 [!DNL Journey Optimizer].

1. 保存您的选择并单击 **[!UICONTROL 创建]**. 新的决策策略被添加在 **[!UICONTROL 决策]**.

   ![](assets/decision-code-based-decision-added.png)

现在，决策策略已创建，您可以在基于代码的体验内容中使用决策属性。 [了解详情](#use-decision-policy)

## 评估顺序 {#evaluation-order}

如上所述，策略包括集合、排名方法和资格约束。

您可以：

* 设置要评估的策略的顺序顺序，
* 合并多个策略，以便一起评估而不是分别评估。

多个策略及其分组决定了策略的优先级和合格优惠的排名。 第一种策略具有最高优先级，同一组内组合策略具有相同的优先级。

例如，您有两个集合，一个在策略A中，另一个在策略B中。该请求用于发送回两个决策项目。 假设策略A中有两个符合条件的优惠，而策略B中有三个符合条件的优惠。

* 如果两种策略是 **未合并** 或按顺序（1和2）排列，第一行将返回第一个策略中前两个符合条件的优惠。 如果第一个策略中没有两个符合条件的优惠，则决策引擎将依次转到下一个策略以查找仍然需要的任意数量的优惠，并且最终将在需要时返回回退。

  ![](assets/decision-code-based-consecutive-strategies.png)

* 如果两个收藏集是 **同时评估**，由于策略A中有两个符合条件的优惠和策略B中有三个符合条件的优惠，因此这五个优惠都将根据各自的排名方法确定的值栈叠在一起。 由于请求了两个选件，因此将返回这五个选件中符合条件的前两个选件。

  ![](assets/decision-code-based-combined-strategies.png)

+++ **具有多种策略的示例**

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

选件1 - 10选件2 - 20选件3 - 30来自战略1,45来自战略2。 两者中的最高值将被考虑在内，因此会考虑45。
选件4 - 40选件5 - 50

排名后的选件现在如下所示：选件5、选件3、选件4、选件2、选件1。

**迭代2：**

已评估策略3选件（选件5、选件6）。 假设结果为：

* 选件5 — 将不进行评估，因为上述结果中已存在该选件。
* 选件6 - 60

排名后的选件现在如下所示：选件5 、选件3、选件4、选件2、选件1、选件6。

+++

## 在代码编辑器中使用决策策略 {#use-decision-policy}

创建决策策略后，便可在以下位置使用： [表达式编辑器](../code-based/create-code-based.md#edit-code). 要实现此目的，请执行以下步骤。

>[!NOTE]
>
>基于代码的体验可利用 [!DNL Journey Optimizer] 具有所有个性化和创作功能的表达式编辑器。 [了解详情](../personalization/personalization-build-expressions.md)

1. 单击+图标。 将添加与决策策略对应的代码。 现在，您可以在该代码中添加所需的所有决策属性。

   ![](assets/decision-code-based-add-decision.png)

   >[!NOTE]
   >
   >此序列将按您希望返回决策策略的次数重复。 例如，如果您选择在 [创建决策](#add-decision)，则同一序列将重复两次。

1. 单击决策策略。 此时将显示决策属性。

   这些属性存储在 **[!UICONTROL 选件]** 目录的架构。 自定义属性存储在 **`_<imsOrg`>** 文件夹和中的标准属性 **`_experience`** 文件夹。 [了解有关优惠目录架构的更多信息](catalogs.md)

   ![](assets/decision-code-based-decision-attributes.png)

1. 单击每个文件夹以将其展开。 将鼠标光标置于所需位置，然后单击要添加属性旁边的+图标。 您可以向代码添加任意数量的属性。

   ![](assets/decision-code-based-add-decision-attributes.png)

1. 要导航回决策策略根目录，请单击文件夹图标。

   ![](assets/decision-code-based-decision-folder.png)

1. 您还可以添加表达式编辑器中可用的任何其他属性，如配置文件属性。

   ![](assets/decision-code-based-decision-profile-attribute.png)
