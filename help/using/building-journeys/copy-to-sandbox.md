---
title: 将历程复制到另一个非道克
description: 了解如何将历程复制到其他非正统
feature: Journeys
topic: Content Management
role: User
level: Intermediate
source-git-commit: f75ed263fd8226a6b5f55bbb50f4aae17cbfe9d4
workflow-type: tm+mt
source-wordcount: '832'
ht-degree: 0%

---

# 将历程复制到其他沙盒 {#copy-to-sandbox}

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_main"
>title="将历程复制到其他沙盒"
>abstract="Journey Optimizer允许您将整个历程从一个沙盒复制到另一个沙盒。 例如，您可以将历程从暂存沙盒环境复制到生产沙盒。 除了历程本身之外，Journey Optimizer还会复制历程所依赖的大多数对象。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_sandbox_details"
>title="沙盒详细信息"
>abstract="选择要将历程复制到的目标沙盒。 只有IMS组织内的沙箱才可用。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_object_details"
>title="对象详细信息"
>abstract="这是您要复制的历程。"

>[!CONTEXTUALHELP]
>id="ajo_journey_copy_dependent_objects"
>title="从属对象"
>abstract="这是历程中使用的关联对象列表。 此列表显示名称、对象类型以及内部Journey Optimizer ID。"

Journey Optimizer允许您将整个历程从一个沙盒复制到另一个沙盒。 例如，您可以将历程从暂存沙盒环境复制到生产沙盒。 除了历程本身之外，Journey Optimizer还复制历程所依赖的大多数对象：消息、区段、预设、架构、事件和操作。 请参阅 [限制](../building-journeys/copy-to-sandbox.md#limitations)

>[!CAUTION]
>
>我们不保证所有链接的元素都会复制到目标沙箱。 我们强烈建议您在发布历程之前进行彻底检查。 这将允许您识别任何潜在的缺失对象。

目标沙箱中复制的对象是唯一的，不会覆盖现有元素。 历程和历程中的任何消息都将以草稿模式传递。 这样，您就可以在在目标沙盒上发布之前执行彻底验证。 复制进程仅通过有关历程和该历程中对象的元数据进行复制。 此过程中不会复制任何配置文件或数据集数据。

要将历程复制到其他沙盒，请执行以下步骤：

1. 在“历程管理”菜单部分，单击 **[!UICONTROL Journeys]**. 将显示历程列表。

2. 搜索要复制的历程，单击 **更多操作** 图标（历程名称旁边的三个圆点），然后单击 **复制到沙盒**.

   ![](assets/copy-sandbox1.png)

   的 **复制到沙盒** 屏幕。

   ![](assets/copy-sandbox2.png)

3. 选择 **Target沙盒** 中。 只有IMS组织内的沙箱才可用。

4. 查看 **从属对象** 中。 这是历程中使用的关联对象列表。 此列表显示名称、对象类型以及内部Journey Optimizer ID。

5. 单击 **复制** 按钮，以开始将历程复制到目标沙箱。

   ![](assets/copy-sandbox3.png)

   复制过程开始，并显示每个对象的进度。 复制过程会因历程的复杂性和需要复制的对象数量而异。 如果遇到错误，将为相关对象显示一条消息。

   ![](assets/copy-sandbox4.png)

6. 复制完成后，单击 **关闭**.

7. 访问目标沙盒，并对所有复制的对象进行彻底检查。

## 复制流程和限制 {#limitations}

我们不保证所有链接的元素都会复制到目标沙箱。 我们强烈建议您进行彻底检查。 识别任何潜在的缺失对象，并在发布历程之前手动创建它们。

将复制以下对象：

* 区段

   一个区段只能从一个沙盒复制到另一个沙盒。 复制区段后，该区段将无法在目标沙箱中编辑。

* 架构

   将复制此历程中使用的架构。

* 消息

   历程中使用的物理消息（电子邮件或推送消息）。 不会检查消息中用于个性化的字段是否完整。 不会复制内容块。

* 历程 — 画布详细信息

   画布上历程的表示形式，包括历程中的对象，如条件、操作、事件、读取区段等。 跳转活动将从副本中排除。

* 活动

   将复制历程中使用的事件和事件详细信息。

* 操作

   将复制历程中使用的操作和操作详细信息。

不会复制预设。 系统会根据消息类型和预设名称，自动选择目标沙箱上可能最接近的匹配项。 如果在目标沙盒上未找到预设，则预设复制将失败。 这将意味着消息副本也将失败，因为消息需要预设才能进行设置。 在这种情况下，需要为消息的正确渠道至少创建一个预设，才能使副本正常工作。

对于方案、合并策略和区段，当第二次尝试复制这些对象时，将只引用它们。 它们将被视为已存在的对象，并将再次复制。 这意味着这些对象只能复制一次。

在Adobe Journey Optimizer引用架构、合并策略和区段之前，需要经过五分钟的延迟，才能在画布中看到错误。 等待五分钟，这些参考资料将可用。

