---
solution: Journey Optimizer
product: journey optimizer
title: 暂停历程
description: 了解如何暂停和恢复实时历程
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="限量发布版" type="Informative"
keywords: 发布，历程，实时，有效性，检查
source-git-commit: 341f818d84264e3cb57563466866fdf43ebc401c
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 3%

---

# 暂停历程 {#journey-pause}

您可以暂停实时历程，执行所有需要的更改，然后随时重新恢复它们。 历程最长可暂停14天。 <!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. -->历程在暂停期结束时自动恢复。 您也可以[手动](#journey-resume-steps)恢复它。


>[!AVAILABILITY]
>
>此功能仅面向一部分组织（限量发布）。要获得访问权限，请与 Adobe 代表联系。


## 主要优点 {#journey-dry-run-benefits}

暂停和恢复历程允许暂停实时历程，并且不影响客户体验，从而为营销人员提供了更好的控制和灵活性。 暂停后，不会发送任何通信，并且用户档案将保持暂停状态，直到历程恢复。

此功能降低在错误或更新（例如：更改消息内容）期间发送意外消息的风险，支持更安全的历程管理，并提高从业者的信心。 直接在UI中查看暂停的历程及其状态可进一步提高透明度和操作敏捷性。

>[!CAUTION]
>
>暂停和恢复历程的权限仅限于具有&#x200B;**[!DNL Publish journeys]**&#x200B;高级权限的用户。 在[本节](../administration/permissions-overview.md)中了解有关管理[!DNL Journey Optimizer]用户访问权限的更多信息。

## 护栏和建议

* 历程版本最长可暂停14天。
* 暂停的历程会以与实时历程相同的方式纳入所有业务规则中。
* 当用户档案到达操作活动时，将会在暂停的历程中“丢弃”用户档案。 如果他们在旅程暂停期间坚持等待并在恢复后退出，则将继续旅程，而不会被丢弃。
* 即使是在暂停后，随着事件继续处理，这些事件也将计入每秒的历程事件数配额，之后将形成单一形式的限制。
* 已进入历程但在暂停期间被放弃的用户档案仍将被计为可参与的用户档案。
* 当配置文件在暂停的历程中保留时，在恢复时配置文件属性会刷新
* 条件仍会在暂停的历程中执行，因此，如果历程因数据质量问题而暂停，则可以使用错误数据评估操作节点之前的任何条件。
* 对于基于受众的增量读取受众历程，请考虑暂停的持续时间。 例如，对于每日历程，如果暂停并在当月2日恢复，则在6日运行将获取从1日到6日符合条件的所有用户档案。 这不适用于受众资格或基于事件的历程（如果在暂停期间收到受众资格或事件，则这些事件将被丢弃）。
* 暂停的历程计入实时历程配额。
* 历程全局超时仍适用于暂停的旅程。 例如，如果某个用户档案在历程中持续90天且历程暂停，则此用户档案仍将在第91天退出历程。
* 如果配置文件保留在历程中，并且此历程在几天后自动恢复，则配置文件将继续该历程并且不会被丢弃。 如果要删除它们，必须停止旅程。
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## 如何暂停历程 {#journey-pause-steps}

您可以暂停任何实时历程。

要暂停历程，请执行以下步骤：

1. 打开要暂停的历程。
1. 单击历程画布右上角的&#x200B;**...更多**&#x200B;按钮，然后选择&#x200B;**暂停**。

   ![暂停历程按钮](assets/pause-journey-button.png)

1. 选择如何管理当前位于历程中的配置文件。

   ![暂停历程选项](assets/pause-confirm.png){width="50%" align="left"}

   您可以：

   * 保留配置文件 — 配置文件将等待历程恢复
   * 放弃配置文件 — 将在下一个操作节点从历程中排除配置文件

1. 单击&#x200B;**暂停**&#x200B;按钮确认。

历程最长可暂停14天。

## 如何恢复暂停的历程 {#journey-resume-steps}

暂停的历程可以随时手动恢复。

要结束历程暂停并开始再次收听历程事件，请执行以下步骤：

1. 打开要恢复的历程。
1. 单击历程画布右上角的&#x200B;**...更多**&#x200B;按钮，然后选择&#x200B;**继续**。

   历程切换到&#x200B;**恢复**&#x200B;状态。 从&#x200B;**恢复**&#x200B;到&#x200B;**实时**&#x200B;状态的过渡可能需要一些时间：必须恢复所有配置文件，历程才能重新&#x200B;**实时**。




