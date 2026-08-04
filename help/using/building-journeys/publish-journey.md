---
solution: Journey Optimizer
product: journey optimizer
title: 发布历程
description: 了解如何在Adobe Journey Optimizer中发布旅程、创建新版本、管理旅程状态以及了解重新发布要求。
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: 发布，历程，实时，有效性，检查
exl-id: e0ca8aef-4f1d-4631-8c34-1692d96e8b51
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Hhvwpfq0phAjvzIGgv-NMnnhWhYJ-PpLOL0F4Q-CnqA
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0bbbbf94550d4cb762ecca300932620c8d3da50e
workflow-type: tm+mt
source-wordcount: 1823
ht-degree: 14%

---

# 发布您的历程 {#publishing-the-journey}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何发布历程以使其上线，包括先决条件、发布流程、版本管理和重新发布要求。

>[!ENDSHADEBOX]

发布历程会激活该历程：它移至&#x200B;**[!UICONTROL 实时]**&#x200B;状态，可供新配置文件进入并切换到只读模式。 您无法发布包含错误的历程。

>[!NOTE]
>
>在保存或发布旅程时，Journey Optimizer会验证旅程有效负载的总大小，并在接近或超过限制时发出警告或阻止发布。 在[历程有效负载大小验证](../start/guardrails.md#journey-payload-size)中了解详情。

➡️ [通过观看视频了解此功能](#video)

## 发布之前 {#before-you-publish}

发布之前，请确保您的历程满足以下先决条件：

* **无验证错误** — 您无法发布包含错误的历程。 [首先测试您的历程](testing-the-journey.md)，然后[对任何活动错误进行故障排除](../building-journeys/troubleshooting.md#activity-errors)。
* **发布权限** — 发布需要&#x200B;**[!DNL Publish journeys]**&#x200B;高级权限。 了解有关[管理访问权限](../administration/permissions-overview.md)的更多信息。
* **有效负载在限制内** — 历程有效负载必须在配置的限制内（默认为4 MB）。 请参阅[历程有效负载大小验证](../start/guardrails.md#journey-payload-size)。
* **已获得批准** — 如果您的历程受批准策略的约束，请在发布之前请求并获得批准。 [了解详情](../test-approve/gs-approval.md)。

>[!TIP]
>
>在发布之前，请使用一个可用的测试选项验证您的历程：
>
>* [Simulation](simulate-journey-gs.md) — 使用模拟用户进行测试，而不使用Adobe Experience Platform中的持久性测试配置文件。
>* [测试模式](testing-the-journey.md) — 在Adobe Experience Platform中使用标记为测试配置文件的持久性配置文件进行测试。
>* [试运行](journey-dry-run.md) — 使用实际生产数据进行测试，而不联系配置文件。

## 发布过程 {#journey-publication}

发布历程的步骤详述如下：

1. 验证历程是否有效且没有错误，以及它是否满足上述[先决条件](#before-you-publish)。

1. 要发布历程，请单击右上角下拉菜单中的&#x200B;**[!UICONTROL 发布]**&#x200B;选项。

   >[!NOTE]
   >
   > 如果您的历程受审批策略的约束，则必须请求审批以发布历程。 [了解详情](../test-approve/gs-approval.md)

   历程工具栏中的![发布按钮以激活历程](assets/journeyuc1_18.png)

发布历程时，它处于&#x200B;**只读**&#x200B;模式。 在只读模式下，您只能修改活动标签和描述、历程名称和历程描述。 如果您需要对已发布的历程进行额外的修改，请创建历程的[新版本](journey-ui.md#journey-filter)。

### 历程状态 {#journey-statuses}

发布后，历程将经历几种状态：

* **[!UICONTROL 实时]** — 历程已发布，用户档案可以进入该历程。
* **[!UICONTROL 已关闭]** — 发布新版本时自动结束的先前版本。 禁止进入。
* **[!UICONTROL 已完成]** — 历程已根据其结束条件完成。 有关何时将历程视为已完成的确切定义，请参阅[历程如何结束](end-journey.md#journey-finished-definition)。

### 停止历程 {#stop-journey}

当您停止历程时，历程将永久停止。 流经历程的所有个人将永久停止，并且历程将停止允许新条目。 如果您需要再次运行历程，请复制它并发布新历程。 有关历程如何结束的更多信息，请参阅[历程如何结束](end-journey.md)。

### 重新发布要求 {#republishing}

在某些情况下，必须重新发布历程才能使更改或资产保持有效：

>[!IMPORTANT]
>
>* 如果对历程消息中使用的优惠决策进行了更改，则需要取消发布该历程并重新发布。 这可确保将更改纳入历程的消息中，并且消息与最新更新一致。
>
>* Assets/图像在任何片段/内联消息中首次发布后最多可在投放内容中2年（730天）内访问。 在此到期期限（730天后的任何时间）后需要重新发布，才能在随后2年内保持可访问状态。 在首次发布后730天内完成的任何重新发布都不会将资产/图像的过期时间延长到接下来的730天。

## 历程版本 {#journey-versions}

在历程列表中，所有历程版本在显示时都带有版本号。 搜索历程时，当应用程序首次打开时，最新版本会显示在列表顶部。 然后，您可以定义所需的排序方式，应用程序会将其保留为用户首选项。 历程的版本也显示在历程版本界面的顶部，位于画布上方。

![历程版本列表显示已发布版本和草稿版本](assets/journeyversions1.png)

>[!NOTE]
>
>通常，对于历程的所有活动版本，同一历程中无法同时存在多个用户档案。 如果启用了重新进入，则用户档案可以重新进入历程，但只有在完全退出该历程的上一个实例后才能重新进入历程。 [了解详情](entry-management.md)。

### 创建历程的新版本 {#journey-create-new-version}

如果您需要修改到实时历程，请创建历程的新版本。 要创建现有历程的新版本，请执行以下步骤：

1. 打开实时历程的最新版本，单击&#x200B;**[!UICONTROL 创建新版本]**&#x200B;并确认。

   ![为复制历程创建新版本对话框](assets/journeyversions2.png)

   >[!NOTE]
   >
   >您只能从历程的最新版本创建新版本。

1. 进行修改，单击&#x200B;**[!UICONTROL 发布]**&#x200B;并确认。

从历程发布的那一刻起，个人将开始转入历程的最新版本。 已进入先前版本的用户将停留在该版本中，直到完成该历程。 如果稍后重新进入同一历程，则将进入最新版本。

可以逐个单独停止历程版本。 历程的所有版本具有相同的名称。

当您发布新版本的历程时，先前版本会自动结束并切换到&#x200B;**已关闭**&#x200B;状态。 无法再进入该历程。 即使您停止了最新版本，先前版本仍会保持关闭状态。


>[!NOTE]
>
>特定护栏和限制适用于历程的版本控制。 请参阅[此页面](../start/guardrails.md#journey-versions-g)以了解详情。


## 常见问题 {#faq}

**为什么我无法发布历程？**

最常见的原因是历程包含验证错误 — 您无法发布包含错误的历程。 其他阻止程序包括超过[有效负载大小限制](../start/guardrails.md#journey-payload-size)、缺少&#x200B;**[!DNL Publish journeys]**&#x200B;权限或挂起[审批](../test-approve/gs-approval.md)。 请参阅[发布之前](#before-you-publish)和[活动错误疑难解答](../building-journeys/troubleshooting.md#activity-errors)。

**旅程发布后可以编辑吗？**

已发布的历程处于只读模式。 您只能更改活动标签和描述、历程名称和历程描述。 对于任何其他更改，[创建历程的新版本](#journey-create-new-version)。

**发布新版本时，历程中已有的用户档案会发生什么情况？**

新配置文件流入最新版本。 先前版本中已存在的配置文件将一直保留到完成；如果它们稍后重新输入，则进入最新版本。 以前的版本会自动切换到&#x200B;**[!UICONTROL 已关闭]**，并且不接受任何新条目。 请参阅[历程版本](#journey-versions)。

**如何重新运行已停止的历程？**

停止历程是永久性的。 要再次运行它，请复制它并发布新历程。 查看[停止历程](#stop-journey)。

**更改优惠决策或更新资产后，是否需要重新发布？**

是的。 如果更改历程消息中使用的优惠决策，请取消发布并重新发布历程，以便应用更改。 Assets和图像会在首次发布后730天过期；之后会重新发布以使其可访问。 请参阅[重新发布要求](#republishing)。

**我是否可以发布需要批准的历程？**

如果您的历程受审批策略的约束，则必须在发布之前请求审批。 [了解有关批准的更多信息](../test-approve/gs-approval.md)。

## 相关主题 {#related-topics}

* [测试您的历程](testing-the-journey.md) — 在发布之前使用测试用户档案验证您的历程
* [历程模拟](simulate-journey-gs.md) — 在发布之前验证模拟用户的历程
* [历程试运行](journey-dry-run.md) — 在不联系用户档案的情况下使用实际生产数据进行测试
* [疑难解答](../building-journeys/troubleshooting.md#activity-errors) — 解决活动和发布错误
* [历程如何结束](end-journey.md#journey-finished-definition) — 了解历程完成和状态
* [用户档案进入管理](entry-management.md) — 配置用户档案如何进入并重新进入历程
* [历程护栏和限制](../start/guardrails.md#journeys-guardrails-journeys) — 查看发布和版本控制护栏

## 操作方法视频 {#video}

在此视频中了解如何发布历程：

>[!VIDEO](https://video.tv.adobe.com/v/3424998?quality=12)

+++ AI知识参考

本节包含结构化知识，用于支持与本主题相关的解释、检索和问答。

要全面了解相关信息，应将此信息与本页上的文档相结合。 这两个源都不是独立的；页面描述了功能，而本节提供了其他上下文来帮助消除术语、意图、适用性和约束条件的歧义。

* **TL；DR：**&#x200B;本页介绍如何发布Adobe Journey Optimizer旅程、管理旅程版本，以及了解旅程上线后应用的限制。

**意图：**
* 发布历程以使其上线并可用于用户档案输入
* 在发布之前验证历程有效性并解决错误
* 创建新版本的实时历程以进行修改
* 了解在发布历程后应用的只读限制
* 永久停止历程或管理版本之间的过渡

**术语表：**
* **历程版本**：历程的编号迭代；创建新版本以修改实时历程，而不会中断正在进行的配置文件&#x200B;*（产品特定）*
* **已关闭状态**：发布新版本时，以前历程版本自动进入的状态；任何新配置文件都不能进入已关闭历程&#x200B;*（产品特定）*
* **审批策略**：在发布历程之前需要明确审批的可选治理工作流&#x200B;*（产品特定）*

**护栏：**
* 无法发布包含错误的历程。
* Journey Optimizer会在保存和发布时验证历程有效负载的总大小；如果超过限制，可能会阻止发布。
* 发布后，历程处于只读模式；只能编辑标签、描述和历程名称。
* 只能从历程的最新版本创建新版本。
* 历程停止后，将永久停止该历程；必须复制历程才能再次运行。
* 自首次发布起，已交付内容中的Assets和图像最多可在730天内访问；在这段时间后，需要重新发布。
* 如果历程消息中使用的优惠决策发生更改，则必须取消发布并重新发布历程。
* 特定护栏适用于历程版本控制（请参阅护栏页面）。

**术语：**
* 规范名称：发布历程 — 缩写：无 — 变体：激活历程，上线
* 同义词： &quot;Publish&quot; = &quot;activate&quot; = &quot;go live&quot;
* 请勿混淆：停止（紧急停止所有配置文件）≠关闭新入口（手动正常关闭；现有配置文件完成）≠已关闭状态（发布新版本时自动关闭，或手动关闭新入口）

**常见问题解答：**
* **问：历程发布后是否可以编辑该历程？**  — 只能更改标签、描述和历程名称。 要进行其他修改，请创建历程的新版本。
* **问：发布新版本后，旧历程版本中的用户档案会发生什么情况？**  — 以前版本中已存在的配置文件将一直保留到完成；新配置文件将输入最新版本。
* **问：我是否可以重新发布已关闭的历程版本？**  — 不。 关闭以前的版本后，即使停止了最新版本，它也会保持关闭状态。
* **问：如果历程中使用的优惠决策发生更改，我应该怎么做？**  — 取消发布历程并重新发布以合并更新的优惠决策。
* **问：发布前是否需要批准？**  — 仅当历程受审批策略约束时；在这种情况下，必须首先请求审批。

+++
