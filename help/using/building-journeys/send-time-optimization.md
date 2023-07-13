---
solution: Journey Optimizer
product: journey optimizer
title: 发送时间优化
description: 了解如何在消息中优化发送时间参数
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发送时间，发送，消息，优化，历程，人工智能，智能
exl-id: ec604e91-4c7f-459c-b6ff-d825919e7181
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 36%

---

# 发送时间优化{#send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_disabled"
>title="关于发送时间优化"
>abstract="Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。"

Adobe Journey Optimizer 的发送时间优化功能由 Adobe 的 AI 服务提供支持，可以预测发送电子邮件或推送消息的最佳时间，从而根据历史打开率和点击率最大限度地提高参与度。使用我们的机器学习模型安排每个用户的个性化发送时间，以提高消息的打开率和点击率。

发送时间优化模型会摄取您的Adobe Journey Optimizer数据，并查看用户级别的打开（针对电子邮件和推送）和点击（针对电子邮件）率，以确定客户何时最有可能参与您的消息传送。 发送时间优化需要至少一个月的消息跟踪数据才能提出有根据的建议。 对于每个用户，系统将使用以下得分自动选择最佳时间：

* 一周中每天的最佳时刻以最大限度地提高参与度
* 一周中最佳的一天，可最大限度地提高参与度
* 一周中最佳一天中最佳的一小时，最大化参与度

无论您是在说得分还是训练，模型都有所不同。 培训最初每周进行，然后每季度进行。 评分最初为每周，然后是每月。

* 训练 — 用于生成得分的算法的开发
* 评分 — 根据经过训练的模型，将评分应用于个人资料

此信息存储在用户的配置文件中，并在历程执行中引用，以告知Adobe Journey Optimizer何时发送消息。

>[!CAUTION]
>
>此功能与突发模式不兼容。

## 激活发送时间优化{#activate-send-time-optimization}

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_email"
>title="激活发送时间优化"
>abstract="通过选择相应的单选按钮，选择是针对电子邮件打开操作还是针对电子邮件点进操作进行优化。您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

>[!CONTEXTUALHELP]
>id="jo_bestsendtime_push"
>title="激活发送时间优化"
>abstract="推送消息默认为打开选项，因为点击不适用于推送消息。 您还可以为“发送于下一个”选项输入一个值，选择限定系统使用的发送时间。"

通过选择电子邮件或推送消息的 **发送时间优化** 切换活动参数。

![](../building-journeys/assets/jo-message5.png)

对于电子邮件，通过选择相应的单选按钮来选择是优化电子邮件打开次数，还是优化电子邮件点进次数。 推送消息默认为打开选项，因为点击不适用于推送消息。 

您还可以通过为输入一个值，选择将系统使用的发送时间包括在内。 **发送于下一个** 选项。 如果你选择“六小时”作为值， [!DNL Journey Optimizer] 将检查每个用户配置文件，并在旅程执行时间后的6小时内选择最佳发送时间。
