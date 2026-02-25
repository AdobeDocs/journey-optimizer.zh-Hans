---
title: 历程仲裁排名公式
description: 了解如何创建公式来对历程进行仲裁排序，从而根据规则和上下文为每个用户档案选择最佳历程。
feature: Journeys, Decisioning
role: User
level: Intermediate
version: Journey Orchestration
badge: label="有限发布版" type="Informative"
source-git-commit: fe6e8221201ee813251a46c6603d85f0803873c0
workflow-type: tm+mt
source-wordcount: '1087'
ht-degree: 2%

---

# 使用公式对历程进行排名 {#journey-ranking-formulas}

>[!AVAILABILITY]
>
>此功能当前处于“有限可用”状态。 请联系 Adobe 代表获取访问权限。

[!DNL Adobe Journey Optimizer]可帮助您控制当用户档案符合超出系统允许范围的条件时，可以输入哪些历程。 为此，您可以使用[规则集](rule-sets.md)来定义历程进入或并发的上限。 当用户档案符合条件的历程超过上限允许时，分配给每个历程的优先级将确定选择哪些历程。

您还可以使用&#x200B;**排名公式**&#x200B;来根据历程属性、用户档案属性或AI模型分数动态调整历程的排名，而不是使用优先级。

与静态优先级相比，公式可提供更大的灵活性。 例如，您可以提升金会员的历程。

<!--
>[!NOTE]
>
>Journey ranking formulas follow the same guardrails as decisioning ranking formulas (nesting depth, rule string size). [Learn more about Decisioning guardrails & limitations](../experience-decisioning/decisioning-guardrails.md#ranking-formulas).-->

## 创建排名公式 {#create-journey-ranking-formula}

要为历程创建排名公式，请执行以下步骤。

1. 访问&#x200B;**[!UICONTROL 业务流程排名]**&#x200B;部分，然后选择&#x200B;**[!UICONTROL 排名公式]**&#x200B;选项卡。 此时将显示之前创建的公式列表。

1. 单击&#x200B;**[!UICONTROL 创建公式]**。

1. 指定公式名称，并根据需要添加说明。

   ![包含名称和描述字段的公式详细信息窗格](assets/journey-formula-details.png){width="80%"}


   >[!NOTE]
   >
   >排名对象是将应用排名公式的实体。 默认情况下，排名对象设置为&#x200B;**[!UICONTROL 历程]**。

   <!--
    Selecting a formula entity specifies which type of item—such as journeys or other entities—the ranking formula will apply to. This determines the context in which the formula operates, allowing you to define rules that influence how those items are ranked.-->

1. （可选）单击&#x200B;**[!UICONTROL 选择AI模型]**&#x200B;以设置将用作构建排名公式的引用的模型。

<!--
    >[!NOTE]
    >
    >[Personalized optimization models](../experience-decisioning/ranking/personalized-optimization-model.md) using continuous metrics are not supported with the AI formula builder.

    Every time you refer to a model score when defining your formula below, the AI model that you selected will be used. [Learn more on AI models](../experience-decisioning/ranking/ai-models.md)-->

1. 在&#x200B;**[!UICONTROL 标准1]**&#x200B;部分中，通过执行以下操作来指定要将排名得分应用于哪些历程：

   * 选择[历程属性](../building-journeys/journey-properties.md)（如历程名称、标记、优先级或其他历程属性）；
   * 选择逻辑运算符；
   * 添加匹配条件 — 您可以键入/选择值，或选择配置文件属性。

   ![标准1部分具有历程属性、运算符和匹配条件](assets/journey-formula-criterion-1.png){width="70%"}

1. （可选）您可以指定其他元素以将标准的匹配条件细化为true。

   ![用于优化匹配条件的其他条件](assets/journey-formula-additional-condition.png){width="70%"}

   例如，您定义了&#x200B;*标准1*，例如&#x200B;*历程标签*&#x200B;包含&#x200B;*忠诚度*。 此外，您还可以添加其他条件，例如&#x200B;*忠诚度状态*&#x200B;等于&#x200B;*Gold*，则&#x200B;*标准1*&#x200B;为true。

1. 创建表达式，将排名得分分配给满足以上定义条件的历程。 您可以引用以下任意一项：
   * 变量：
      * 历程优先级，它是在[创建历程](../building-journeys/journey-gs.md)时分配给历程的手动值；
      * 你选择在上面选择的AI模型得出的分数；
   * 属性：
      * 个人资料上可能存在的任何属性，如任何外部派生的倾向分数；
      * 历程属性；
   * 可以自由格式分配的静态值；
   * 以上各项的组合。

   ![使用变量、属性或静态值分配排名得分的表达式生成器](assets/journey-formula-expression.png){width="70%"}

1. 单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;可根据需要多次添加一个或多个条件。 其逻辑如下：
   * 如果第一个标准对于给定的决策项为true，则它优先于下一个标准。
   * 如果不为true，则决策引擎将转到第二个标准，依此类推。

1. 定义所有标准后，在最后一个字段中，您可以构建一个表达式，该表达式将分配给不符合上述标准的所有历程。

   不符合任何条件的历程的![表达式字段](assets/journey-formula-criteria-not-met.png){width="70%"}

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以完成排名公式。

您现在可以从列表中选择此公式以查看其详细信息，然后对其进行编辑或删除。 然后，当您配置规则集时，它便可用。 [了解如何操作](#assign-formula-to-ruleset)

### 排名公式示例 {#journey-ranking-formula-example}

请参考下面的示例。

+++示例1：使用历程优先级或基于历程标记的AI分数

![排名公式：营销标记使用历程优先级](assets/journey-formula-ex-1.png){width="60%"}

如果历程具有“营销”标记，则排名分数是历程优先级。

![排名公式：促销标记使用AI模型得分](assets/journey-formula-ex-2.png){width="60%"}

如果历程具有“促销”标记，则排名分数是AI模型分数。

+++

+++示例2：按用户档案状态提高忠诚度历程


![排名公式：具有金会员状态的忠诚度标记使用历程优先级加5](assets/journey-formula-ex-3.png){width="60%"}

如果历程具有“忠诚度”标记，并且用户档案的忠诚度状态为“金级”，则使用的排名分数是历程优先级加5。

![排名公式：具有银牌状态的忠诚度标记使用历程优先级加2](assets/journey-formula-ex-4.png){width="60%"}

如果历程具有“忠诚度”标记，并且用户档案的忠诚度状态为“白银”，则排名得分为历程优先级加2。

如果不符合上述任何条件，则使用的排名分数是历程优先级。

+++

### 使用代码编辑器 {#journey-ranking-formula-code-editor}

若要以&#x200B;**PQL语法**&#x200B;表达排名公式，请使用屏幕右上角的专用按钮切换到代码编辑器。 有关如何使用PQL语法的更多信息，请参阅[专用文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html?lang=zh-Hans)。

>[!CAUTION]
>
>此操作将阻止您返回此公式的默认生成器视图。

然后，您可以利用历程属性、配置文件属性和静态值来构建排名公式。

<!--The code editor is similar to the one used in Decisioning ranking formulas. [Learn more](../experience-decisioning/ranking/ranking-formulas.md#ranking-code-editor)-->

## 将公式分配给规则集 {#assign-formula-to-ruleset}

要使用公式对历程进行排名，您需要将其分配给规则集。

>[!NOTE]
>
>公式在规则集级别分配，而不是在单个历程中分配。

1. 从&#x200B;**[!UICONTROL 业务规则]**&#x200B;菜单中，创建要用于历程仲裁的规则集。 [了解如何操作](rule-sets.md#Create)

1. 确保选择&#x200B;**[!UICONTROL 历程]**&#x200B;域。

   ![已选择历程域的规则集属性](assets/journey-formula-rule-set-journey.png){width="60%"}

1. 在规则集属性中，将&#x200B;**[!UICONTROL 排名方法]**&#x200B;设置为&#x200B;**[!UICONTROL 公式]**（而不是默认的&#x200B;**[!UICONTROL 优先级]**）。

1. 从下拉列表中选择您创建的排名公式。

   ![从下拉列表中选择排名公式的规则集](assets/journey-rule-set-formula.png){width="60%"}

1. 创建要添加到规则集的历程上限规则。 [了解如何操作](journey-capping.md#create-rule)

1. 保存规则集。

现在，该公式已分配给规则集。 然后，您可以将该规则集应用于历程。

## 将规则集应用于历程 {#assign-rule-set-to-journey}

要将规则集分配给历程，请执行以下步骤。

1. 创建或打开要为其分配规则集的历程。 [了解如何创建历程](../building-journeys/journey-gs.md)

1. 在历程属性中，从下拉列表中选择规则集。  [了解如何操作](journey-capping.md#apply-capping)。

   >[!NOTE]
   >
   >一次只能将一个规则集应用于历程。

1. 保存历程。

当应用上限时，使用此规则集的所有历程将按所选公式进行排名。

要监视规则集和排名公式的执行方式，请参阅概述报表中的[历程上限和冲突](../reports/channel-report-cja.md#rule-sets)部分。

<!--
## Reporting {#reporting}

Reporting for journey arbitration helps you understand how rule sets and ranking formulas perform:

* **Exclusions** – Whether journeys were excluded from users and which rule set (and reason) prevented entry.
* **Rule set performance** – For each rule set, metrics such as journey enters, journey exclusions, journey engagement, and other optimization metrics.
* **Cross-journey view** – Time-based view of profiles across journeys (e.g. journey enters, failures, exclusions) to see the impact of capping and ranking.

Use these reports to validate that your formulas and caps are behaving as intended and to tune ranking logic over time.-->

