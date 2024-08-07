---
solution: Journey Optimizer
product: journey optimizer
title: 发送时间优化
description: 了解如何在消息中优化参数发送时间
feature: Journeys, Activities, Email, Push, Send Time Optimization
topic: Content Management
role: User
level: Intermediate
keywords: 发送时间，发送，消息，优化，历程， AI，智能
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '482'
ht-degree: 26%

---

# 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

Adobe Journey Optimizer的发送时间优化功能由Adobe的AI服务提供支持，可以根据历史打开率和点击率，预测发送电子邮件或推送消息的最佳时间，从而最大化参与度。 使用我们的机器学习模型安排每个用户的个性化发送时间，以增加消息的打开率和点击率。

发送时间优化模型会摄取您的Adobe Journey Optimizer数据，并查看用户级别的打开率（适用于电子邮件和推送）和点击率（适用于电子邮件），以确定客户何时最有可能参与您的消息传送。 发送时间优化需要至少一个月的消息跟踪数据才能提出明智的建议。 对于每个用户，系统将使用以下得分自动选择最佳时间：

* 一周中每天的最佳时刻以最大限度地提高参与度
* 一周中最佳的一天，可最大限度地提高参与度
* 一周中最佳时刻的最佳时刻以最大限度地提高参与度

无论您是要打分还是要训练，这个模型都不尽相同。 培训最初每周进行，然后每季度进行。 得分最初是每周评分，然后每月评分。

* 训练 — 开发用于生成得分的算法
* 评分 — 根据训练后的模型将评分应用到个人用户档案

此信息存储在用户的配置文件中，并在历程执行时引用，以告知Adobe Journey Optimizer何时发送消息。

## 激活发送时间优化{#activate-send-time-optimization}

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
