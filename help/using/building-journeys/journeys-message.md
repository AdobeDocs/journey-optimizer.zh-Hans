---
solution: Journey Optimizer
product: journey optimizer
title: 将内置渠道操作添加到历程
description: 了解如何将内置渠道操作添加到历程
feature: Journeys, Activities, Channels Activity
topic: Content Management
role: User
level: Intermediate
keywords: 历程，消息，推送，短信，电子邮件，应用程序内， Web，内容卡，基于代码的体验
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: tm+mt
source-wordcount: '1268'
ht-degree: 19%

---

# 使用内置渠道操作 {#add-a-message-in-a-journey}

>[!CONTEXTUALHELP]
>id="ajo_message_activity"
>title="内置渠道操作"
>abstract="Journey Optimizer 附带内置操作功能。您只需在历程中添加出站（电子邮件、短信（SMS/MMS）、推送）或入站（应用程序内、网页、基于代码的体验、信息卡）活动，并定义设置和内容。然后将在历程的上下文中执行和发送它。"

[!DNL Journey Optimizer]附带内置渠道操作功能。 您只需在历程中添加出站（电子邮件、短信（SMS/MMS）、推送）或入站（应用程序内、网页、基于代码的体验、信息卡）活动，并定义设置和内容。然后将在历程的上下文中执行和发送它。

>[!NOTE]
>
>您还可以设置特定操作以向您发送消息。 [了解详情](#recommendation)

要将内置渠道操作添加到历程，请执行以下步骤。

1. 通过[事件](general-events.md)或[读取受众](read-audience.md)活动开始您的历程。

1. 从调色板的&#x200B;**操作**&#x200B;部分，将出站（**电子邮件**、**推送**、**短信**）或入站（**应用程序内**、**Web**、**基于代码的体验**、**内容卡**）活动拖放到画布中。

   ![](assets/journey-web-activity.png)

1. 配置您的活动。

   * 了解创建消息内容的详细步骤，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../email/create-email.md">
      <img alt="潜在客户" src="../assets/do-not-localize/email.jpg">
      </a>
      <div><a href="../email/create-email.md"><strong>创建电子邮件</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../push/create-push.md">
      <img alt="不频繁" src="../assets/do-not-localize/push.jpg">
      </a>
      <div>
      <a href="../push/create-push.md"><strong>创建推送通知<strong></a>
      </div>
      <p>
      </td>
      <td>
      <a href="../sms/create-sms.md">
      <img alt="验证" src="../assets/do-not-localize/sms.jpg">
      </a>
      <div>
      <a href="../sms/create-sms.md"><strong>创建短信(SMS/MMS)</strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

   * 了解创建集客操作的详细步骤，如下所示：

     <table style="table-layout:fixed">
      <tr style="border: 0;">
      <td>
      <a href="../in-app/create-in-app.md">
      <img alt="潜在客户" src="../assets/do-not-localize/in-app.jpg">
      </a>
      <div><a href="../in-app/create-in-app.md"><strong>创建应用程序内消息</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../web/create-web.md">
      <img alt="潜在客户" src="../assets/do-not-localize/web-create.jpg">
      </a>
      <div><a href="../web/create-web.md"><strong>创建Web体验</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../content-card/create-content-card.md">
      <img alt="潜在客户" src="../assets/do-not-localize/sms-config.jpg">
      </a>
      <div><a href="../content-card/create-content-card.md"><strong>创建内容卡</strong>
      </div>
      <p>
      </td>
      <td>
      <a href="../code-based/create-code-based.md">
      <img alt="不频繁" src="../assets/do-not-localize/web-design.jpg">
      </a>
      <div>
      <a href="../code-based/create-code-based.md"><strong>创建基于代码的体验<strong></a>
      </div>
      <p>
      </td>
      </tr>
      </table>

     >[!NOTE]
     >
     >每个入站消息活动都具有3天&#x200B;**等待**&#x200B;活动。 [了解详情](../building-journeys/wait-activity.md#auto-wait-node)

## 推荐 {#recommendation}

[!DNL Journey Optimizer]附带内置消息功能。 但是，通过自定义操作，您可以配置第三方系统的连接以发送消息或API调用。

* 如果您使用第三方系统来发送消息，则可以创建自定义操作。 [了解详情](../action/action.md)

* 如果您使用的是Campaign和Journey Optimizer，请参阅以下部分：

   * [[!DNL Journey Optimizer]和Campaign v7/v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer]和Campaign Standard](../action/acs-action.md)

## 更新实时内容{#update-live-content}

您可以在实时历程中更新内置渠道操作的内容。

为此，请打开您的实时历程，选择渠道活动，然后单击&#x200B;**编辑内容**。

![](assets/add-a-message2.png)

但是，您无法更改个性化中使用的属性，无论这些属性是配置文件属性还是上下文数据（来自事件或历程属性）。

如果修改了上下文数据，将显示以下错误消息：ERR_AUTHORING_JOURNEYVERSION_201

如果修改了配置文件属性，将显示以下错误消息：ERR_AUTHORING_JOURNEYVERSION_202

请注意，对于应用程序内活动，可以在历程实时期间对内容进行任何更改，但无法修改应用程序内触发器。

## 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

>[!NOTE]
>
>默认情况下，此功能未启用。 请联系您的Adobe代表以将其激活。
>
>发送时间优化功能仅适用于电子邮件和推送渠道。

### 关于发送时间优化 {#about-send-time}

Adobe Journey Optimizer的发送时间优化功能由Adobe的AI服务提供支持，可根据历史打开率和点击率，预测发送&#x200B;**电子邮件**&#x200B;或&#x200B;**推送消息**&#x200B;的最佳时间，从而最大限度地提高参与度。 使用我们的机器学习模型安排每个用户的个性化发送时间，以增加消息的打开率和点击率。

发送时间优化模型会摄取您的Adobe Journey Optimizer数据，并查看用户级别的打开率（适用于电子邮件和推送）和点击率（适用于电子邮件），以确定客户何时最有可能参与您的消息传送。 发送时间优化需要至少一个月的消息跟踪数据才能提出明智的建议。 对于每个用户，系统将使用以下得分自动选择最佳时间：

* 一周中每天的最佳时刻以最大限度地提高参与度
* 一周中最佳的一天，可最大限度地提高参与度
* 一周中最佳时刻的最佳时刻以最大限度地提高参与度

无论您是要打分还是要训练，这个模型都不尽相同。 培训最初每周进行，然后每季度进行。 得分最初是每周评分，然后每月评分。

* 训练 — 开发用于生成得分的算法
* 评分 — 根据训练后的模型将评分应用到个人用户档案

此信息存储在用户的配置文件中，并在历程执行时引用，以告知Adobe Journey Optimizer何时发送消息。

### 常见问题解答 {#faq-send-time}

+++ 发送时间优化可以做什么？ 它如何处理新用户档案？ 它是否将发送分散到6/12/24小时的窗口内？

发送时间优化会尝试预测与客户互动的最佳时间，并优化电子邮件的打开/点击率。 得分采用每个配置文件`3*7*24`属性的格式。 `7*24`属性描述向收件人发送电子邮件的预测最佳时间排名，3用于优化电子邮件打开率、电子邮件点击率和推送打开率。

+++

+++在哪里可以查看每个用户档案的预期发送时间？

您可以在&#x200B;**配置文件**&#x200B;界面中看到总体分数。 对于三组168分中的每组，排名从–83升至84。 排名越高，选择与收件人交互的时间就越好。 由于您可以定义历程的开始和持续时间，因此最佳排名(84)可能不会落入该时间范围内。 在这种情况下，我们建议选择具有最高排名值的小时。

+++


+++有哪些报表可用？

访问您的旅程，单击右上方的&#x200B;**查看报告**&#x200B;按钮，然后选择左侧的&#x200B;**历程**&#x200B;选项卡。 [了解详情](../reports/journey-global-report-cja.md)

+++

+++发送时间优化数据如何影响用户档案丰富度？

发送时间优化会将得分/属性添加到每个用户档案，但不会创建新用户档案。

+++

### 激活发送时间优化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活发送时间优化"
>abstract="通过选择相应的单选按钮，选择是针对电子邮件打开操作还是针对电子邮件点进操作进行优化。您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活发送时间优化"
>abstract="推送消息默认为打开选项，因为点击不适用于推送消息。您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

从活动参数中选择&#x200B;**发送时间优化**&#x200B;开关，对电子邮件或推送消息启用发送时间优化。

![](../building-journeys/assets/jo-message5.png)

对于电子邮件，选择是优化电子邮件打开次数，还是通过选择相应的单选按钮优化电子邮件点进次数。 推送消息默认为打开选项，因为点击不适用于推送消息。

您还可以通过在&#x200B;**Send within the next**&#x200B;选项中输入值，选择将系统使用的发送时间包括在内。 如果您选择“6小时”作为值，[!DNL Journey Optimizer]将检查每个用户配置文件，并从历程执行时间起6小时内选择最佳发送时间。

**如果最佳时间在窗口之外，会发生什么情况？**

让我们以以下设置为例：

* 单击时优化
* 操作定于上午10点开始
* 窗口为3小时

用户档案可以有一个最佳打开时间，该时间在窗口之外。 例如，John的最佳点击打开时间是下午5点。

在用户档案级别，存在一周中每个小时的分数。 在此示例中，电子邮件将始终在窗口中发送。 在运行时，系统会检查该时段（上午10点开始的3小时时段）内的得分列表。 然后，系统比较10、11和中午的分数，并选择最高分。 此时会发送电子邮件。
