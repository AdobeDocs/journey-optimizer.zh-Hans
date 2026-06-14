---
solution: Journey Optimizer
product: journey optimizer
title: 创建 LINE 消息
description: 了解如何在Journey Optimizer中创建LINE消息
feature: Line
topic: Content Management
role: User
level: Beginner
exl-id: a93d4dc9-f0e9-400c-b9a4-6cdac84390fd
TQID: https://experienceleague.adobe.com/OgI9e9LWYpO8nXHQXoDK-y0ys-EpHJzaFRHx9V9pAus
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: e09fc1e6-407c-418f-adc5-e2ffe8b8986e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 8f016fe08e76f896eeb71b96e582e4e7e8fc3c9f
workflow-type: tm+mt
source-wordcount: 782
ht-degree: 4%

---

# 创建 LINE 消息 {#create-line}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;将LINE操作添加到历程或营销活动中，并生成个性化内容（从文本和贴纸到图像、视频、位置和Flex消息），以便您能够在线吸引客户。

>[!ENDSHADEBOX]

## 添加LINE消息 {#create-line-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_line"
>title="LINE操作"
>abstract="LINE渠道操作会在用户档案达到历程的此步骤时向用户档案发送LINE消息。 标签在历程画布中标识活动，并且操作引用定义交付内容的LINE配置。 **优化**&#x200B;部分可以包含内容实验或定位规则，**多语言**&#x200B;部分可以投放多种语言的内容，并且&#x200B;**超时或错误**&#x200B;部分可以定义在操作失败时的替代路径。"
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/orchestrate-journeys/about-journey-building/journey-action#add-action" text="渠道操作入门"

浏览以下选项卡，了解如何在营销活动或历程中添加LINE消息。

>[!BEGINTABS]

>[!TAB 向历程添加LINE消息]

1. 打开您的历程，然后从调色板的&#x200B;**操作**&#x200B;部分拖放&#x200B;**LINE**&#x200B;活动。

   ![](assets/jo-line-1.png)

1. 提供有关消息的基本信息（标签、说明、类别），然后选择要使用的消息配置。

   有关如何配置历程的详细信息，请参阅[此页面](../building-journeys/journey-gs.md)

   默认情况下，**[!UICONTROL 配置]**&#x200B;字段已预填充用户用于该渠道的最后一个配置。

您现在可以从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计LINE消息的内容，如下所述。

>[!TAB 向营销活动添加LINE消息]

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 从&#x200B;**[!UICONTROL 属性]**&#x200B;部分，编辑营销活动的&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮，从可用Adobe Experience Platform受众列表中定义要定位的受众。 [了解详情](../audience/about-audiences.md)。

1. 在&#x200B;**[!UICONTROL 身份命名空间]**&#x200B;字段中，选择要使用的命名空间，以便识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 行]**，然后选择或创建新配置。

   在[此页面](line-configuration.md)中了解有关LINE配置的更多信息。

   ![](assets/campaign-line-1.png)

1. 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;开始配置内容试验并创建处理以测量其性能并为目标受众确定最佳选项。 [了解详情](../content-management/content-experiment.md)

1. 在&#x200B;**[!UICONTROL 操作跟踪]**&#x200B;部分中，指定是否要跟踪短信消息中的链接点击次数。

1. 营销活动旨在按特定日期或循环频率执行。 在[本节](../campaigns/create-campaign.md#schedule)中了解如何配置促销活动的&#x200B;**[!UICONTROL 计划]**。

1. 从&#x200B;**[!UICONTROL 操作触发器]**&#x200B;菜单中，选择短信消息的&#x200B;**[!UICONTROL 频率]**：

   * 一次
   * 每日
   * 每周
   * Month

您现在可以从&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计文本消息的内容，如下所述。

>[!ENDTABS]

## 定义LINE内容{#line-content}

Adobe Journey Optimizer支持LINE的以下消息类型：

* **文本**：发送纯文本或格式化的文本消息。
* **贴纸**：加入LINE的本机贴纸以添加字符和表现力。
* **图像**：附加图像以增强视觉吸引力。
* **视频**：共享视频内容以进行动态通信。
* **位置**：使用地图发送位置信息。
* **模板**：利用预定义的模板进行一致的消息传递。
* **Flex消息**：使用基于JSON的Flex消息创建内容丰富的复杂布局。

通过直接编辑JSON内容可配置这些消息类型，从而允许实施动态和个性化的消息传递策略。

要配置LINE内容，请执行以下步骤。

1. 在历程或营销策划配置屏幕中，单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮以配置文本消息内容。

1. 单击&#x200B;**[!UICONTROL 编辑代码]**&#x200B;以编辑JSON内容。

1. 使用个性化编辑器定义内容、添加个性化和动态内容。 您可以使用任何属性，例如配置文件名称或城市。 您还可以定义条件规则。 浏览到以下页面，了解有关个性化编辑器中的[个性化](../personalization/personalize.md)和[动态内容](../personalization/get-started-dynamic-content.md)的更多信息。

1. 单击&#x200B;**[!UICONTROL 保存]**&#x200B;并在预览中检查您的消息。

1. 使用&#x200B;**[!UICONTROL 模拟内容]**&#x200B;预览LINE消息内容和个性化内容。 [了解详情](send-line.md)

执行测试并验证内容后，您可以向受众发送LINE消息。 这些步骤在[此页面](send-line.md)中详述

发送后，您可以在促销活动或历程报表中测量LINE的影响。 有关报告的更多信息，请参考[此章节](../reports/campaign-global-report-cja.md)。
