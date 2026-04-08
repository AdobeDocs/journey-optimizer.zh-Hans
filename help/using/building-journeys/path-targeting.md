---
solution: Journey Optimizer
product: journey optimizer
title: 路径定位
description: 了解如何在历程中使用路径定位
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 定位，规则，历程，路径，优化，个性化
exl-id: b30ce5c9-a0e2-4601-97a3-5bec648368e4
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '799'
ht-degree: 7%

---

# 利用路径定位 {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="什么是后备路径？"
>abstract="回退路径可在没有符合条件的定向规则时，让受众进入备用路径。</br>如果您未选择此选项，任何不符合定向规则的受众将不会进入回退路径，而是直接退出历程。"

>[!AVAILABILITY]
>
>此功能当前处于“有限可用”状态。 要请求访问权限，请与 Adobe 代表联系。

定位规则允许您根据特定受众区段<!-- depending on profile attributes or contextual attributes-->确定客户必须符合哪些特定规则或资格才有资格进入历程路径之一。

与实验（随机分配给定路径）不同，定位是确定性的，可确保正确的受众或用户档案进入指定的路径。

<!--
With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.
-->

要在历程中设置定位，请执行以下步骤。

1. 从&#x200B;**[!UICONTROL 业务流程]**&#x200B;部分中，将&#x200B;**[!UICONTROL 优化]**&#x200B;活动拖放到历程画布中。

1. 添加可选标签，这对于在报告和测试模式日志中标识活动很有用。

1. 从&#x200B;**[!UICONTROL 方法]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 定位规则]**。

   优化活动中的![定位规则选择](assets/journey-optimize-targeting.png){width=60%}

1. 单击&#x200B;**[!UICONTROL 创建定位规则]**。

1. 单击&#x200B;**[!UICONTROL 创建规则]** > **[!UICONTROL 新建]**，然后使用规则生成器定义您的条件。

   ![用于创建定位标准的规则生成器界面](assets/journey-targeting-create-rule.png){width=100%}

   例如，为忠诚度计划的金会员定义规则(`loyalty.status.equals("Gold", false)`)，为其他会员定义规则(`loyalty.status.notEqualTo("Gold", false)`)。

   金会员和非金会员的![忠诚度状态定位规则](assets/journey-targeting-rule.png)

1. 您还可以单击&#x200B;**[!UICONTROL 创建规则]** > **[!UICONTROL 选择规则]**&#x200B;以选择从&#x200B;**[!UICONTROL 规则]**&#x200B;菜单创建的现有定位规则。 [了解详情](../experience-decisioning/rules.md)

   ![从“规则”菜单中选择现有的定位规则](assets/journey-targeting-select-rule.png){width=70%}

   在这种情况下，组成规则的公式将简单地复制到历程活动中。 从&#x200B;**[!UICONTROL 规则]**&#x200B;菜单对该规则进行的任何后续更改将不会影响历程的副本。

   >[!AVAILABILITY]
   >
   >[通过专用](../experience-decisioning/rules.md#create)菜单创建定位规则[!DNL Journey Optimizer]目前可供已购买Decisioning附加产品的组织使用，其他组织也可应要求使用这些规则（限量发布）。
   >
   >此容量将逐步推广到所有客户。 在此期间，请联系您的Adobe代表以获取访问权限。

1. 添加规则后，您仍可以对其进行修改。 选择&#x200B;**[!UICONTROL 编辑内联]**&#x200B;以使用规则生成器随时更新它，或选择&#x200B;**[!UICONTROL 选择规则]**&#x200B;以选取其他现有规则。

   ![编辑内联或选择用于修改定位规则的规则选项](assets/journey-targeting-modify-rule.png){width=100%}

   >[!NOTE]
   >
   >编辑内联规则不会影响其源自的现有规则。

1. 根据需要选择&#x200B;**[!UICONTROL 启用回退路径]**&#x200B;选项。 此操作会为不符合以上定义的任何定位规则的受众创建回退路径。

   >[!NOTE]
   >
   >如果不选择此选项，则任何不符合定位规则的受众都不会进入回退路径并退出历程。

1. 单击&#x200B;**[!UICONTROL 创建]**&#x200B;以保存您的定位规则设置。

1. 返回历程，拖放特定操作以自定义每个路径。 例如，创建一个电子邮件，为金会员提供个性化优惠，并为所有其他会员提供短信提醒。

   ![历程路径，其中包含Gold成员的电子邮件以及其他成员的短信](assets/journey-targeting-paths.png)

1. 如果您在定义规则设置时选择了&#x200B;**[!UICONTROL 启用回退内容]**&#x200B;选项，请为自动添加的回退路径定义一个或多个操作。

   不合格配置文件的![回退路径配置](assets/journey-targeting-fallback.png){width=70%}

1. 或者，在超时或错误的情况下使用&#x200B;**[!UICONTROL 添加替代路径]**&#x200B;以定义在出现问题时的替代操作。 [了解详情](using-the-journey-designer.md#paths)

1. 为对应于由定位规则设置定义的每个组的每个操作设计适当的内容。

   在此示例中，设计一封电子邮件，其中为金会员提供特殊优惠，并为其他会员提供短信提醒。<!--You can seamlessly navigate between the different contents for each action. ![Content design panel for targeting rule actions](assets/journey-targeting-design.png)-->

1. [发布](publish-journey.md)您的历程。

历程处于实时状态后，将处理为每个区段指定的路径，以便Gold成员使用电子邮件选件输入路径，而其他成员使用短信提醒输入路径。

使用历程报告跟踪旅程的成功情况。 [了解详情](../reports/journey-global-report-cja.md#targeting)

## 定位规则用例 {#uc-targeting}

以下示例显示如何将&#x200B;**[!UICONTROL Optimize]**&#x200B;活动与&#x200B;**[!UICONTROL 定位规则]**&#x200B;方法结合使用，以个性化不同子受众的路径。

+++特定于区段的渠道

金会员状态忠诚会员可以通过电子邮件接收个性化优惠，而所有其他会员将被定向到短信提醒。

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![特定于区段的渠道，针对电子邮件为金会员而短信为其他金会员](assets/journey-optimize-targeting-uc-segment.png)

+++

+++基于行为的定位

已打开电子邮件但未单击的客户会收到推送通知，而完全未打开的客户则会收到短信。

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![通过推送或短信回退进行的电子邮件参与基于行为的定位](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++购买历史记录定位

最近购买过产品的客户可能会进入一个简短的“感谢您+交叉销售”路径，而那些没有购买历史的客户则会进入一个更长的培养历程。

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![针对购买者的交叉销售路径和非购买者的培养路径的购买历史记录](assets/journey-optimize-targeting-uc-purchase.png)

+++
