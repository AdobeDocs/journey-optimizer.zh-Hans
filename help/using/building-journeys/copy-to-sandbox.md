---
solution: Journey Optimizer
product: journey optimizer
title: 将历程复制到另一个沙盒
description: 了解如何将历程复制到另一个沙盒
feature: Journeys
topic: Content Management
role: User, Developer
level: Intermediate
keywords: 沙盒，历程，复制，环境
exl-id: 8c63f2f2-5cec-4cb2-b3bf-2387eefb5002
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 20%

---

# 将历程复制到另一个沙盒 {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="将历程复制到另一个沙盒"
>abstract="可以使用 Journey Optimizer 将整个历程从一个沙盒复制到另一个沙盒。例如，您可以将历程从暂存沙盒环境复制到生产沙盒。除了历程本身，Journey Optimizer 还会复制历程所依赖的大部分对象。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="沙盒详细信息"
>abstract="选择您要将历程复制到的目标沙盒。只有您组织内的沙盒可用。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="对象详细信息"
>abstract="这就是您要复制的历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="依赖对象"
>abstract="这是在历程中使用的关联对象的列表。此列表显示名称、对象类型以及内部 Journey Optimizer ID。"

可以使用 Journey Optimizer 将整个历程从一个沙盒复制到另一个沙盒。例如，您可以将历程从暂存沙盒环境复制到生产沙盒。 除了历程本身，Journey Optimizer还复制历程依赖的大部分对象：受众、界面（即预设）、架构、事件和操作。 有关复制对象的更多详细信息，请参阅此 [部分](#limitations).

>[!CAUTION]
>
>我们不保证将所有链接的元素复制到目标沙盒中。 我们强烈建议您在发布历程之前执行彻底检查。 这将允许您标识任何可能缺少的对象。

目标沙盒中复制的对象是唯一的，不存在覆盖现有元素的风险。 历程和历程中的任何消息都会以草稿模式引入。 这允许您在目标沙盒上发布之前执行彻底验证。 复制过程仅复制有关历程的元数据和该历程中的对象。 在此过程中不会复制任何用户档案或数据集数据。

要将历程复制到另一个沙盒，请执行以下步骤：

1. 在历程管理菜单部分，单击 **[!UICONTROL 历程]**. 将显示历程列表。

2. 搜索要复制的历程，单击 **更多操作** 图标（历程名称旁边的三个圆点）并单击 **复制到沙盒**.

   ![](assets/copy-sandbox1.png)

   此 **复制到沙盒** 屏幕上会显示。

   ![](assets/copy-sandbox2.png)

3. 选择 **Target沙盒** 从下拉字段中。 只有您组织内的沙盒可用。

4. 查看 **依赖对象** 部分。 这是在历程中使用的关联对象的列表。此列表显示名称、对象类型以及内部 Journey Optimizer ID。

5. 单击 **复制** 按钮以开始将历程复制到目标沙盒。

   ![](assets/copy-sandbox3.png)

   复制过程开始，并显示每个单独对象的进度。 复制过程因历程的复杂性以及需要复制的对象数量而异。 如果遇到错误，则会显示相关对象的消息。

   ![](assets/copy-sandbox4.png)

6. 复制完成后，单击 **关闭**.

7. 访问目标沙盒并对所有复制的对象执行彻底检查。

## 复制流程和限制 {#limitations}

可能无法将所有链接的元素复制到目标沙盒。 Adobe强烈建议您执行彻底检查。 识别任何潜在的缺少对象，并在发布历程之前手动创建它们。

将复制以下对象：

* 受众

  一个受众只能从一个沙盒复制到另一个沙盒。 复制受众后，该受众就无法在目标沙盒中编辑。

* 架构

  将复制此历程中使用的架构。

* 消息

  历程中使用的渠道操作活动。 消息中用于个性化的字段不检查完整性。 不会复制内容块。

* 历程 — 画布详细信息

  画布上历程的表示形式，包括历程中的对象，如条件、操作、事件、读取受众等。 将从副本中排除“跳转”活动。

* 活动

  旅程中使用的事件和事件详细信息将会复制。

* 操作

  旅程中使用的操作和操作详细信息已复制。

曲面（即预设）不会被复制。 系统根据消息类型和表面名称，自动选择目标沙盒上最接近的匹配项。 如果在目标沙盒上未找到表面，则表面复制将失败。 这意味着邮件副本也将失败，因为邮件需要一个可用于设置的界面。 在这种情况下，为了使副本正常工作，需要为消息的正确渠道创建至少一个表面。

对于架构、合并策略和受众，当这些对象第二次尝试复制时，将仅引用它们。 它们将被视为已存在的对象，并将再次被复制。 这意味着这些对象只能被复制一次。

Adobe Journey Optimizer会延迟五分钟才能引用架构、合并策略和受众，并且不会在画布中看到错误。 等待五分钟，这些引用将可用。
