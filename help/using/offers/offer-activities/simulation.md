---
title: 创建模拟
description: 了解如何模拟将在给定投放位置提供哪些优惠，以验证您的决策逻辑
feature: Decision Management
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: e213261a1c2cb3421d59ba6c44c832a5f5929cd1
workflow-type: tm+mt
source-wordcount: '885'
ht-degree: 12%

---

# 创建模拟 {#create-simulations}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation"
>title="模拟产品建议决策"
>abstract="通过模拟，可模拟对于某个给定的投放位置，将哪些产品建议投放到某个测试轮廓。这样测试和细化您的产品建议的各个版本即可不影响目标收件人。"

## 关于模拟 {#about-simulation}

要验证决策逻辑，您可以模拟将哪些选件交付到给定投放位置的测试用户档案。

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

这样测试和细化您的产品建议的各个版本即可不影响目标收件人。

>[!NOTE]
>
>此功能模拟对[!DNL Decisioning] API的单个请求。 了解有关[使用Decisioning API提供优惠](../api-reference/offer-delivery-api/decisioning-api.md)的更多信息。

要访问此功能，请从&#x200B;**[!UICONTROL 决策管理]** > **[!UICONTROL 优惠]**&#x200B;菜单中选择&#x200B;**[!UICONTROL 模拟]**&#x200B;选项卡。

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>由于模拟未生成任何决策事件，因此[上限](../offer-library/creating-personalized-offers.md#capping)计数不受影响。

<!--
➡️ [Discover this feature in video](#video)
-->

## 选择测试轮廓 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="添加测试轮廓"
>abstract="您可通过选择身份标识命名空间以及对应的身份标识值来添加测试轮廓。您必须拥有已经可用的测试轮廓才能将它们用于模拟。"

首先，您需要选择将用于模拟的测试用户档案。

>[!CAUTION]
>
>您必须具有可用的测试用户档案，以模拟将向他们投放哪些优惠。 了解如何[创建测试配置文件](../../audience/creating-test-profiles.md)。

1. 单击&#x200B;**[!UICONTROL 管理配置文件]**。

   ![](../assets/offers_simulation-manage-profile.png)

1. 选择要用于标识测试配置文件的身份命名空间。 在本例中，我们将使用&#x200B;**电子邮件**&#x200B;命名空间。

   >[!NOTE]
   >
   >身份命名空间定义标识符的上下文，例如电子邮件地址或CRM ID。 在本节](../../audience/get-started-identity.md){target="_blank"}中了解有关Adobe Experience Platform身份命名空间[的更多信息。

1. 输入身份值并单击&#x200B;**[!UICONTROL 查看]**&#x200B;列出可用的配置文件。

   ![](../assets/offers_simulation-add-profile.png)

1. 如果要测试不同的配置文件数据，请添加其他配置文件，并保存您的选择。

   ![](../assets/offers_simulation-save-profiles.png)

1. 添加后，所有配置文件都列在&#x200B;**[!UICONTROL 测试配置文件]**&#x200B;下的下拉列表中。 您可以在保存的测试配置文件之间切换以显示每个选定配置文件的结果。

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >选定的配置文件将保留在&#x200B;**[!UICONTROL Simulation]**&#x200B;选项卡中作为测试配置文件列出，从会话到会话，直到使用&#x200B;**[!UICONTROL 管理配置文件]**&#x200B;将其删除为止。

1. 您可以单击&#x200B;**[!UICONTROL 配置文件详细信息]**&#x200B;链接以显示选定的配置文件数据。

## 添加决策范围 {#add-decision-scopes}

现在，选择要在测试用户档案上模拟的优惠决策。

1. 选择&#x200B;**[!UICONTROL 添加决策范围]**。

   ![](../assets/offers_simulation-add-decision.png)

1. 从列表中选择版面。

   ![](../assets/offers_simulation-add-decision-scope.png)

1. 将显示可用的决策。

   * 您可以使用搜索字段来优化选择。
   * 您可以单击&#x200B;**[!UICONTROL 打开优惠决策]**&#x200B;链接以打开您创建的所有决策的列表。 了解有关[决策](create-offer-activities.md)的更多信息。

   选择您选择的决策并单击&#x200B;**[!UICONTROL 添加]**。

   ![](../assets/offers_simulation-add-decision-scope-add.png)

1. 您刚刚定义的决策范围将显示在主工作区中。

   您可以调整要请求的优惠数量。 例如，如果您选择2，则会为此决策范围显示最佳的2个优惠。

   ![](../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >您最多可以请求30个选件。

1. 重复上述步骤以根据需要添加任意数量的决策。

   ![](../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >即使您定义了多个决策范围，也只模拟一个API请求。

## 定义模拟设置 {#define-simulation-settings}

要编辑模拟的默认设置，请执行以下步骤。

1. 单击&#x200B;**[!UICONTROL 设置]**。

   ![](../assets/offers_simulation-settings.png)

1. 在&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;部分中，您可以选择允许跨决策和/或投放位置重复优惠。 这意味着可能会为多个决策/投放分配同一优惠。

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >默认情况下，会为模拟启用所有重复数据删除标记，这意味着决策引擎允许重复项，因此可以在多个决策/投放位置提出相同的建议。 在[本节](../api-reference/offer-delivery-api/decisioning-api.md)中了解有关[!DNL Decisioning] API请求属性的更多信息。

1. 在&#x200B;**[!UICONTROL 响应格式]**&#x200B;部分中，您可以选择在代码视图中包含元数据。 选中相应的选项，然后选择您选择的元数据。 选择&#x200B;**[!UICONTROL 查看代码]**&#x200B;时，它们将显示在请求和响应负载中。 在[查看模拟结果](#simulation-results)部分了解详情。

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >打开该选项时，缺省情况下会选择所有项目。

1. 单击&#x200B;**[!UICONTROL 保存]**。

>[!NOTE]
>
>当前对于模拟数据，只能使用&#x200B;**[!UICONTROL Hub]** API。

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## 查看模拟结果 {#simulation-results}

在添加决策范围并选择测试用户档案后，您可以查看结果。

1. 单击&#x200B;**[!UICONTROL 查看结果]**。

   ![](../assets/offers_simulation-view-results.png)

1. 系统会根据为每个决策选择的配置文件显示最佳可用优惠。

   选择选件以显示其详细信息。

   ![](../assets/offers_simulation-offer-details.png)

1. 单击&#x200B;**[!UICONTROL 查看代码]**&#x200B;以显示请求和响应负载。 [了解详情](#view-code)

1. 从列表中选择另一个用户档案，以显示不同测试用户档案的优惠决策结果。

1. 您可以根据需要多次添加、删除或更新决策范围。

>[!NOTE]
>
>每次更改配置文件或更新决策范围时，都需要使用&#x200B;**[!UICONTROL 查看结果]**&#x200B;按钮刷新结果。

## 查看代码 {#view-code}

1. 使用&#x200B;**[!UICONTROL 查看代码]**&#x200B;按钮显示请求和响应负载。

   ![](../assets/offers_simulation-view-code.png)

   代码视图显示当前用户的开发人员信息。 默认情况下，将显示&#x200B;**[!UICONTROL 响应有效负载]**。

   ![](../assets/offers_simulation-request-payload.png)

1. 单击&#x200B;**[!UICONTROL 响应有效负载]**&#x200B;或&#x200B;**[!UICONTROL 请求有效负载]**&#x200B;在两个选项卡之间导航。

   ![](../assets/offers_simulation-response-payload.png)

1. 要在[!DNL Journey Optimizer]之外使用请求有效负载 — 例如，出于疑难解答目的，请使用代码视图顶部的&#x200B;**[!UICONTROL 复制到剪贴板]**&#x200B;按钮复制该有效负载。

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >将请求或响应负载复制到您自己的代码时，请确保使用有效值替换{USER_TOKEN}和{API_KEY}。 请参阅[Adobe Experience Platform API](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html?lang=zh-Hans){target="_blank"}文档以了解如何检索这些值。

