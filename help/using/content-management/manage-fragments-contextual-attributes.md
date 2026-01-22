---
solution: Journey Optimizer
product: journey optimizer
title: 向已发布的片段添加上下文属性
description: 了解如何向已发布的片段添加上下文属性（限量发布）
feature: Fragments
topic: Content Management
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
source-git-commit: 69efe0254aae3cb067f2c9f89db6aa4fe0a50549
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 4%

---

# 向已发布的片段添加上下文属性 {#adding-contextual-attributes}

>[!AVAILABILITY]
>
>此功能仅适用于特定客户，并涉及重大风险。 与您的Adobe代表确认已为贵组织启用此功能。

默认情况下，不支持向已发布的片段添加新的[个性化属性](../personalization/personalization-build-expressions.md)。 发布片段后，将为所有营销活动和历程锁定配置文件或上下文属性集。

但是，对于选定的客户，可以只将&#x200B;**上下文属性**&#x200B;添加到已发布的片段。

>[!WARNING]
>
>将个性化属性添加到已发布的片段时，验证过程不太严格，并且可能无法检测到错误。 这可能会导致使用该片段的历程和营销活动大规模发生意外中断。

## 护栏和限制 {#limitations}

* 确保当前使用片段的所有历程和营销活动都可以处理新的上下文属性。
* 无法将配置文件属性添加到已发布的片段。 仅支持上下文属性。
* 上下文属性必须手动输入到代码编辑器中 — 无法从个性化编辑器UI中选择它们。
* 向实时片段添加个性化属性时，验证会放松，这意味着可能无法检测到错误，并可能导致大规模意外中断。
* 发布后，任何错误都将立即影响使用该片段的所有通信。

## 添加上下文属性 {#add-contextual-attributes}

要向已发布的片段添加上下文属性，请执行以下步骤。

>[!IMPORTANT]
>
>仅当您完全[了解对引用片段的历程和营销活动的影响](#limitations)时才继续。

1. 导航到&#x200B;**[!UICONTROL 内容管理]** > **[!UICONTROL 片段]**。

1. 选择已发布的片段，然后单击&#x200B;**[!UICONTROL 修改]**&#x200B;以创建草稿版本。

   ![](assets/fragment-live-modify.png){width="70%" align="left"}

1. 单击&#x200B;**[!UICONTROL 编辑]**&#x200B;以打开片段内容编辑器。

1. 在个性化编辑器中切换到&#x200B;**[!UICONTROL 代码编辑器]**&#x200B;或&#x200B;**[!UICONTROL 高级模式]**。

1. 使用`{{context.attribute_name}}`语法手动键入或复制粘贴上下文属性：

   `promotionCode`属性的示例：

   ```
   {{context.promotionCode}}
   ```

   >[!CAUTION]
   >
   >仔细检查属性路径是否准确。 可能无法检测到错误，并且可能会大规模中断历程或营销活动通信。

1. 保存更改。

1. 确认后，单击&#x200B;**[!UICONTROL 发布]**&#x200B;以启用更改。

>[!NOTE]
>为避免历程和营销活动之间出现意外中断，您可以在非生产环境中测试上下文属性路径。

## 相关主题 {#related-topics}

* [管理片段](manage-fragments.md)
* [编辑片段](manage-fragments.md#edit-fragments)
* [API 触发的营销活动](../campaigns/api-triggered-campaigns.md)
* [个性化语法](../personalization/personalization-syntax.md)

