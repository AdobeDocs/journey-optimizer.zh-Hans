---
title: 迁移到历程内联创作
description: 了解如何迁移消息
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: f98ef26fa9c6075c852d33d19c796351296a3f94
workflow-type: tm+mt
source-wordcount: '1673'
ht-degree: 0%

---


# 内联创作迁移概述{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="了解有关新的内联创作消息的更多信息"
>abstract="从2022年7月25日开始，直接从历程创作消息。 现有消息会自动迁移到新模型。 迁移后需要执行其他操作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-messages-steps.html" text="迁移步骤"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="了解正在发生的事情"
>abstract="从2022年7月25日开始，直接从历程创作消息。 正在迁移您的环境。 迁移后需要执行其他操作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-messages-steps.html" text="迁移步骤"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="了解如何迁移消息"
>abstract="从2022年7月25日开始，直接从历程创作消息。 现在，现有消息已迁移到新模型。 作为历程从业者，现在需要其他操作。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-messages-steps.html" text="迁移步骤"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="了解如何迁移消息"
>abstract="从2022年7月25日开始，消息菜单会消失，并且会直接从历程创作消息。 如果要在历程中重复使用旧版消息，需要将其另存为模板。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html#save-as-template" text="将消息另存为模板"

Adobe Journey Optimizer将发布一项新功能，以改进您为Journey Optimizer渠道（电子邮件、推送、短信）创作内容的方式。 作为Journey Optimizer从业人员，您现在可以直接从历程创建和创作消息。

此功能需要迁移使用消息的现有历程。 在此页面中，您将找到有关此更改以及所需步骤的必要信息。

有关您作为Journey Optimizer执业者的角色和职责的更多信息，请参阅此 [页面](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## 重要的注意事项{#keys}

* **我是否受到影响**:如果您从 **消息** 菜单，并在您的历程中使用它们。 如果您使用的是第三方系统(例如Adobe Campaign)，则不受此迁移的影响。

* **产品更改**:在GA（7月25日），将在每个历程中创建和管理渠道内容。 的 **消息** 菜单（在左侧导航中）不再可用([了解更多](../rn/inline-messages.md#change))。 我们将继续为您的现有历程进行迁移。

* **时间轴**:每个区域在夜间(通过多个 [迭代](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **必需操作**:将为您执行历程的自动转换。 话虽如此，我们需要你的帮助。 详细了解此 [页面](../rn/inline-messages-steps.md).

* **弃用**:9月6日之后，所有仍在使用旧版消息的历程都将停止，并将在稍后删除。

## 优点和产品更改{#change}

Adobe的愿景是不断简化产品，以提供高效、优化的用户流。 这种创建消息的新方式可以更加简化用户流程。

我们设计了这一新工作流，以便将内容集中到一个位置（即直接使用的位置）。

现在，内容的创建操作将直接在历程中执行。 立即 **好处** 您获得：

* 在单个流程中使用Journey Optimizer渠道加快旅程构建。
* 通过在历程中的所有电子邮件、推送和短信内容之间无缝切换，快速实现内容可视化。
* 通过画布中的上下文个性化改进了电子邮件和推送的流程。
* 历程报告可集中显示详细的渠道报告信息。

以下是 **产品更改** 由此新功能带来：

<table>
<tr>
<th>迁移前</th>
<th>迁移后</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>之前，您使用 <strong>消息</strong> 菜单。 </p></td>
<td><img src="assets/inline-migration-after.png"><p>现在， <strong>消息</strong> 菜单中，将不再可用。 </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>然后，您创建了一个历程，添加了 <strong>消息</strong> 活动，并选择之前创建的消息。</p></td>
<td><img src="assets/inline-migration-after2.png"><p>现在，您只需将所需的渠道操作活动（电子邮件、短信、推送）添加到历程中即可。 在活动中，您可以直接配置消息参数并访问内容编辑器。</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>以前，可以在消息级别和历程级别访问报告。 您必须在消息执行选项卡和历程报表之间导航。</p></td>
<td><img src="assets/inline-migration-after3.png"><p>现在，所有报表都集中在历程级别。 这可改善导航和用户体验。 当您在一个历程中有多封电子邮件时，您可以使用 <strong>操作</strong> 下拉菜单查看相关报表。
</p></td>
</tr>
</table>

在GA（7月25日），此新用户流适用于所有新历程。 的 **消息** 菜单中，将不再可用。

## 迁移时间表{#iterations}

需要进行迁移，才能使用 **消息** 包含内联创作操作的历程。 将为您执行历程的自动转换。 话虽如此，我们需要你的帮助。

每个区域在夜间通过多次迭代进行迁移。 以下是迁移时间表：

* 2022年7月25日：GA — 第1次迭代
* 2022年8月1日：第2次迭代
* 2022年9月5日：3次迭代
* 2022年9月6日：弃用

为什么我们需要多次迭代？

在迭代过程中，我们会遍历每个历程并尽可能迁移它们。 在某些情况下，我们不希望自动迁移：当历程处于实时或关闭状态（即其中仍可能包含用户档案）。 在这些情况下，我们会要求您执行一项操作，然后下一个迭代将迁移这些在上一迭代中无法迁移的历程。

## 常见问题解答 {#faq}

### 如何通知我更改？{#inform}

Adobe在首次迭代之前与您通信。

这项变化经过几次反复修改后，在一夜之间得到部署。 了解详情 [迭代](../rn/inline-messages.md#inline-authoring).

产品内通知也会告知您，这些通知会显示在历程屏幕上：

* 更改部署前

   ![](assets/inline-migration-banner1.png)

* 迭代期间

   ![](assets/inline-migration-banner2.png)

* 迭代后

   ![](assets/inline-migration-banner3.png)

   迭代后， **检查状态** 按钮。 这允许您以JSON格式查看所有历程及其各自的迁移状态。 请参阅 [部分](../rn/inline-messages.md#status).

* 横幅消失后，您就可以走了。 您无需再执行任何操作。

### 迁移过程是什么？{#process}

对于非实时或已关闭的历程，迁移是完全自动的。 我们不希望影响实时或已关闭的历程，以避免任何生产影响。 我们要求您发布我们为您创建的新版本。

客户组织的所有沙箱将同时处理。 在更改部署期间，将执行以下操作：

**任何不使用消息的历程**

这些组件不受更改的影响。 迁移仅定向使用消息的历程。 但是，您仍然能够通过以下URL访问历程中未使用的消息：https://experience.adobe.com/#/@[组织]/sname:[沙盒]/journey-optimizer/messages/

**至少使用一条消息起草历程**

消息的草稿版本会在迁移期间进行修改。 他们不再引用消息。 的 **消息** 活动替换为相应的渠道操作活动。 每个渠道参数和内容。

与往常一样，在发布草稿历程之前对其进行测试。

**至少使用一条消息的实时历程**

历程的实时版本会持续运行，以避免对生产产生任何影响。

此历程的新草稿版本将在迁移期间创建。 此新草稿版本是实时版本的副本，但消息将被内联创作的渠道操作替换。 每个渠道操作活动都包括渠道参数和内容。 内容不会丢失。 报告不会丢失。

我们希望您查看此草稿版本、测试并发布该版本，以便该版本成为实时版本。

**已完成或已停止的历程（至少使用一条消息）**

这些历程也将进行迁移。

在查看历程报表时，报表现在更丰富，并包含了以前在消息报表中提供的信息级别。

**使用至少一条消息的已结束历程**

历程的已关闭版本会针对内部的任何用户档案持续运行，以避免对生产产生任何影响。

30天后，已关闭的历程会自动切换到“已完成”状态。 完成后，将在下一次迭代中考虑这些参数。

**多渠道历程**

这些文件不会迁移。 您必须重新创建它们。

### 作为客户，我的操作项目是什么？{#actions}

我们会为您执行历程的自动转换，但需要执行一些步骤。 详细了解此 [页面](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### 如何检查迁移状态？{#status}

单击 **检查状态** 按钮。 将显示以下页面。

![](assets/inline-migration-log.png)

状态报表位于沙盒级别。 此报表包括几个有用的部分：

**migrationStatus**

此部分显示自首次迭代以来的迁移信息。 数字在每次迭代后递增。

* 已迁移：已成功迁移草稿、已完成和已停止的历程数。
* NEW_VERSION_CREATED:迁移的实时历程数。 对于每个实时历程，都会创建一个新的草稿版本：您必须测试并发布此版本。
* 错误：由于失败而未迁移的草稿、已完成和已停止历程的数量。 您需要重新创建它们。
* ERROR_ON_NEW_VERSION_CREATION:因失败而未迁移的实时历程数。 由于失败，未迁移新的草稿历程版本。 尚未为其创建新草稿版本。 您需要手动重新创建它们。

**igilityStatus**

此部分列出上次迭代后的其余项目：

* toMigrate:需要迁移的草稿、已完成和已停止的历程数。
* createNewVersion:要迁移的实时历程数。
* noMigration_live:无需迁移的实时历程数。 此处还列出了已结束的历程。
* noMigration:无需迁移的历程数。

的 **详细信息** 部分提供相关历程的列表，以供上述每个部分使用。

### 此更改会导致服务中断吗？{#interruption}

服务不会中断。

* 在实时历程中：没有影响，它们继续运行。
* 在创作历程上：在迁移期间（夜间），我们强烈建议不要创建、编辑或删除历程。

### 数据会丢失吗？ {#data}

不会丢失数据，也不会对实时历程产生任何影响。 您将可以控制发布更新的历程版本。

### 功能会丢失吗？{#functionality}

您创作消息的方式将会发生更改。 功能不会丢失。

### 迁移过程中是否有环境访问权限？

迁移发生在夜间。 您将能够使用产品。 但请勿创建、编辑或删除历程。

### 是否会继续发送消息？

是的，实时历程继续运行。

### 如何知道迁移已完成？

横幅消失时迁移完成。 请参阅 [部分](../rn/inline-messages.md#inform).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
