---
solution: Journey Optimizer
product: journey optimizer
title: 条件活动
description: 了解条件活动
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: 活动、条件、画布、历程、优化
badge: label="限量发布版" type="Informative"
hidefromtoc: true
hide: true
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
source-git-commit: 19130e9eb5a2144afccab9fa8e5632de67bc7157
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 6%

---

# 优化活动 {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="优化活动"
>abstract="通过&#x200B;**优化**&#x200B;活动，您可以基于特定标准（包括实验、目标选择和特定条件）创建多条路径，由此定义个人在您的历程中的进度情况。"

>[!AVAILABILITY]
>
>此功能为限量发布版。请联系 Adobe 代表以获取访问权限。

通过&#x200B;**优化**&#x200B;活动，您可以根据特定条件（包括试验、定位和特定条件）创建多个&#x200B;**路径**，从而定义个人如何完成您的历程 — 确保最大程度的参与并成功创建高度自定义且有效的历程。

**历程路径**&#x200B;可以包含以下任意内容：

* 通信排序；
* 他们之间的时间；
* 通信数量；
* 或这三个变量的任意组合。

例如，一个路径可能包含一封电子邮件，另一个路径可能包含两封短信消息，第三个路径可能包含一封电子邮件，两个小时的[等待](wait-activity.md)节点，然后是短信消息。

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

通过&#x200B;**优化**&#x200B;活动，您可以：

* 运行[路径实验](#experimentation)
* 在每个历程路径中利用[定位](#targeting)规则
* 将[条件](#conditions)应用到您的路径

![](assets/journey-optimize.png)

历程上线后，系统会根据定义的标准评估用户档案，并根据匹配标准，将用户档案沿历程中的相应路径发送。

## 使用试验 {#experimentation}

通过试验可以基于随机拆分测试不同的路径，以根据预定义的成功量度确定哪个路径的表现最佳。

要在历程中设置试验，请执行以下步骤。

假设您要比较三个路径：

* 一条路径，一封电子邮件；
* 第二条　路径，其Wait节点为两天，且发送电子邮件；
* 第三个路径，其中包含电子邮件，然后是短信消息。

1. 将&#x200B;**[!UICONTROL 优化]**&#x200B;活动拖放到历程画布中。

1. 添加可选标签以在报告和测试模式日志中标识活动。

1. 从&#x200B;**[!UICONTROL 方法]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 试验]**。

   ![](assets/journey-optimize-experiment.png){width=85%}

1. 单击&#x200B;**[!UICONTROL 试验设置]**。

1. 根据需要设计和配置试验。 [了解如何操作](../content-management/content-experiment.md)

   <!--
    ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}
    Replace with appropriate screenshot
    The experiment applies to all the activities in the journey.TBC
   -->

历程开始后，将随机分配用户以沿着不同路径依次访问。 [!DNL Journey Optimizer]跟踪哪些路径可推动更多购买，并提供可操作的分析。

<!--Follow the success of your journey with the [Experimentation journey report](../reports/campaign-global-report-cja-experimentation.md). Is there a report specific to experimentation in journey?-->

### 包含试验的用例 {#uc-experiment}

以下示例显示如何将&#x200B;**[!UICONTROL Optimize]**&#x200B;活动与&#x200B;**[!UICONTROL Experiment]**&#x200B;方法结合使用，以确定哪条路径总体效果最佳。

**渠道效果**

测试通过电子邮件发送第一条消息还是通过短信发送第一条消息是否会提高转化率。

* 使用转化率作为优化量度（例如：购买、注册）。

![](assets/journey-optimize-experiment-uc.png)

**消息频率**

运行试验以检查在一周内发送一封电子邮件还是发送三封电子邮件是否会导致更多购买。

* 使用购买或取消订阅率作为优化量度。

**通信之间的等待时间**

比较24小时等待与跟进前72小时的等待，以确定哪个时间可最大化参与。

* 使用点进率或收入作为优化量度。

## 利用定位 {#targeting}

定位允许您根据特定受众区段<!-- depending on profile attributes or contextual attributes-->确定客户必须符合哪些特定规则或条件才有资格进入历程路径之一。

与实验（随机分配给定路径）不同，定位是确定性的，可确保正确的受众或用户档案进入指定的路径。

通过定位，可以根据以下内容定义特定规则：

* **用户配置文件属性**，如位置(如 地理定位)、年龄或偏好设置。 例如，美国用户看到“金门”促销活动，而法国用户看到“埃菲尔铁塔”促销活动。

* **上下文数据**，如设备类型(如 device-targeting)、时间或会话详细信息。 例如，桌面用户接收桌面优化内容，而移动设备用户接收移动设备优化内容。

* **受众**，可用于包含或排除具有特定受众成员资格的用户档案。

要在历程中设置定位，请执行以下步骤。

1. 将&#x200B;**[!UICONTROL 优化]**&#x200B;活动拖放到历程画布中。

1. 添加可选标签以在报告和测试模式日志中标识活动。

1. 从&#x200B;**[!UICONTROL 方法]**&#x200B;下拉列表中选择&#x200B;**[!UICONTROL 定位]**。

   ![](assets/journey-optimize-targeting.png){width=85%}

1. 单击&#x200B;**[!UICONTROL 创建定位规则]**。

1. 使用规则生成器定义您的标准。 例如，为美国居民制定规则，为法国居民制定规则，为印度居民制定规则。

   ![](assets/journey-targeting-rule.png)

1. 根据需要选择&#x200B;**[!UICONTROL 启用后备内容]**。 后备内容允许受众在没有符合定位规则时接收默认内容。 如果不选择此选项，则任何不符合上面定义的定向规则的受众都不会输入回退路径。

1. 保存定位规则设置。

1. 返回历程，拖放特定操作以自定义每个路径。 例如，您可以为美国居民创建特定电子邮件，为法国居民创建其他电子邮件，等等。

   ![](assets/journey-targeting-paths.png)

1. 为定向规则设置所定义的每个组设计适当的内容。 您可以无缝地在不同路径之间导航。

   ![](assets/journey-targeting-design.png)

   在此示例中，为美国居民设计一条特定路径，为法国居民设计另一条路径，为印度居民设计另一条路径。

一旦历程处于活动状态，将为每个区段指定的路径将进行处理，以便美国居民进入特定路径，法国居民进入其他路径，依此类推。

### 使用案例和定位 {#uc-targeting}

以下示例显示如何将&#x200B;**[!UICONTROL Optimize]**&#x200B;活动与&#x200B;**[!UICONTROL Targeting]**&#x200B;方法结合使用，以个性化不同子受众的路径。

**特定于区段的渠道**

金会员状态忠诚会员可以通过电子邮件接收个性化优惠，而所有其他会员将被定向到短信提醒。

* 使用每个用户档案的收入或转化率作为优化量度。

![](assets/journey-optimize-targeting-uc.png)

**基于行为的定位**

已打开电子邮件但未单击的客户会收到推送通知，而完全未打开的客户则会收到短信。

* 使用点进率或下游转化作为优化量度。

**购买历史记录目标**

最近购买过产品的客户可能会进入一个简短的“感谢您+交叉销售”路径，而那些没有购买历史的客户则会进入一个更长的培养历程。

* 使用重复购买率或参与率作为优化量度。

## 添加条件 {#conditions}

您可以添加条件，以通过根据特定条件创建多个路径来定义个人如何在您的历程中前进。 您还可以配置备用路径来处理超时或错误，以确保获得无缝的体验。

![](assets/journey-condition.png)

在[本节](conditions.md)中了解如何定义条件。

可以使用以下类型的条件：

* [数据Source条件](condition-activity.md#data_source_condition)
* [时间条件](condition-activity.md#time_condition)
* [百分比拆分](condition-activity.md#percentage_split)
* [日期条件](condition-activity.md#date_condition)
* [配置文件上限](condition-activity.md#profile_cap)
