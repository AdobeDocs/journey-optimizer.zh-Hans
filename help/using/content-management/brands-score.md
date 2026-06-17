---
source-git-commit: a281a4d244279a6a1fce6968e4636b86414c4400
workflow-type: tm+mt
source-wordcount: '1029'
ht-degree: 6%

---
由于此文件在此存储库中不存在，并且未批准写入权限，因此提供了所请求的完整更新Markdown文件：

&#x200B;---
title：品牌对齐方式
description：了解如何使用品牌得分创建、验证和管理品牌内内容。
主题：内容管理、人工智能
角色：用户
级别：初学者，中级
exl-id： 01e74670-7431-4791-b98c-12278e6d3332
TQID： https://experienceleague.adobe.com/hs1F6tz-XHYH6u8jO4kspRcX-ftY-SwilqMfcaLhTfg
product_v2：
- 标识：cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label： Journey Optimizer
feature_v2：
- id： dc22c819-3f29-4e91-8b7d-5c6719831141
internal-label：内容管理
- 标识：fe338112-e2ce-4876-8989-fc4d497613f1
internal-label：电子邮件
subfeature_v2：
- id： ea4139d9-3405-4b34-ad6e-c3ca120cc269
internal-label：多语言内容
- 标识：ee5bb250-0884-4d71-86eb-d8489e8bcadd
内部标签：电子邮件设计
- id：fb9a80eb-bebc-492f-a0e9-584595621ebb
internal-label：发布
role_v2：
- id：b69b2659-1057-424e-8fc5-ed9e016dc554
internal-label：用户
level_v2：
- id：b5a62a22-46f7-4f0d-b151-3fc640bef588
internal-label：中级
- 标识：e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
internal-label：初学者
topic_v2：
- id：bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
internal-label：人工智能
- 标识：e1e0219c-f879-479f-8427-888ed2a6e9c2
内部标签：分析
---
# 品牌一致性 {#brands-score}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何根据品牌准则验证电子邮件内容，并使用Adobe Journey Optimizer中的品牌协调得分来评估整体内容质量。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_brand_score"
>title="品牌一致性得分"
>abstract="您的品牌一致性得分衡量的是您的内容遵循品牌指导方针的程度，确保颜色、字体、徽标、图像和写作风格的一致性。"

>[!CONTEXTUALHELP]
>id="ajo_brand_colors"
>title="颜色得分"
>abstract="颜色得分"

>[!CONTEXTUALHELP]
>id="ajo_brand_fonts"
>title="字体得分"
>abstract="字体得分"

>[!CONTEXTUALHELP]
>id="ajo_brand_logos"
>title="徽标得分"
>abstract="徽标得分"

>[!CONTEXTUALHELP]
>id="ajo_brand_suggestions"
>title="AI生成的建议"
>abstract="当在品牌协调或质量评估期间标记内容时，AI Assistant会自动生成更正的替代项，您可以内联查看和应用这些替代项。"

>[!AVAILABILITY]
>
>您必须同意[用户协议](https://www.adobe.com/cn/legal/licenses-terms/adobe-dx-gen-ai-user-guidelines.html){target="_blank"}，然后才能在Adobe Journey Optimizer中使用AI助手。 有关更多信息，请与您的 Adobe 代表联系。

“品牌协调”功能可帮助您创建、查看和管理遵守品牌准则的内容。 它可确保电子邮件促销活动在语气、消息传递和视觉身份方面保持一致，同时在内容上线之前用作质量检查。

## 通过品牌一致性验证内容 {#validate-content}

设置并发布[您的品牌后](brands.md)，请直接在电子邮件促销活动中评估您的品牌一致性分数，以确保您的内容与品牌准则保持一致：

1. 创建您的[电子邮件营销活动](../campaigns/create-campaign.md)。

1. 在Email Designer中打开&#x200B;**[!UICONTROL Brand Alignment]**&#x200B;菜单。

   您的内容会自动根据默认品牌进行评估。 [了解如何分配默认品牌](brands.md)。

   ![](assets/brand-score-1.png)

1. 若要使用其他品牌进行评估，请从&#x200B;**[!UICONTROL 品牌]**&#x200B;下拉菜单中选择该品牌，然后单击&#x200B;**[!UICONTROL 评估得分]**。

   ![](assets/brand-score-2.png)

1. 浏览&#x200B;**[!UICONTROL 书写样式]**&#x200B;或&#x200B;**[!UICONTROL 可视化内容]**&#x200B;以查看有关得分的更多见解。

   ![](assets/brand-score-3.png)

1. 单击![全屏图标获取详细的见解](assets/do-not-localize/Smock_FullScreen_18_N.svg "全屏")图标，查看更多有关您得分的见解。

   ![](assets/brand-score-5.png)

1. 选择任何标记的准则以查看特定反馈和AI生成的建议。 品牌协调会评估以下类别：

   &#x200B;* **[!UICONTROL 正在写入样式]**：
      &#x200B;* **[!UICONTROL 品牌沟通风格]**：定义个性化和情绪基调，以确保所有渠道的品牌声音一致。
      &#x200B;* **[!UICONTROL 品牌消息传递标准]**：有效的营销和促销文本的结构化和格式化规则。
      &#x200B;* **[!UICONTROL 法律合规性标准]**：确保所有通信符合法律要求，包括文本放置和合规性核对清单。

   &#x200B;* **[!UICONTROL 可视内容]**：
      &#x200B;* **[!UICONTROL 摄影标准]**：摄影内容的要求，包括分辨率、构图、光照和文件格式。
      &#x200B;* **[!UICONTROL 插图标准]**：插图的样式参数、行宽、颜色使用方式和文件格式要求。
      &#x200B;* **[!UICONTROL 图标标准]**：图标设计的规范，包括网格系统、描边粗细和大小调整以保持一致性。
      &#x200B;* **[!UICONTROL 使用准则]**：用于图像选择、放置和上下文的最佳实践，以维护品牌标识。



   ![](assets/brand-score-4.png)

1. 对于标记的写入样式问题，请复查显示在每个违规下方的AI生成的建议，然后单击&#x200B;**[!UICONTROL 应用]**&#x200B;以替换内嵌标记的内容，或将其关闭以保留原始文本。 [了解有关应用AI生成的建议的更多信息](#apply-suggestions)。

1. 进行更改后手动重新评估内容，以刷新对齐分数。

## 验证内容质量 {#validate-quality}

>[!NOTE]
>
>内容质量评估与品牌指南无关。 即使从下拉菜单中选择了品牌，其指导方针也不会应用于质量检查。 品牌选择仅与品牌关联度评分相关。

除了品牌协调之外，您还可以评估总体内容质量，以确定可读性、内容一致性和有效性方面的潜在问题，而不受品牌指南的影响。

要评估内容质量，请执行以下操作：

1. 创建您的[电子邮件营销活动](../campaigns/create-campaign.md)。

1. 在Email Designer中打开&#x200B;**[!UICONTROL Brand Alignment]**&#x200B;菜单。

   ![](assets/brand-score-1.png)

1. 单击&#x200B;**[!UICONTROL 评估得分]**&#x200B;以生成品牌一致性和内容质量得分。

   ![](assets/brand-score-2.png)

1. 导航到&#x200B;**[!UICONTROL 整体质量]**&#x200B;选项卡，以查看您的内容质量见解和推荐。

   ![](assets/brand-score-6.png)

1. 单击![全屏图标获取详细的见解](assets/do-not-localize/Smock_FullScreen_18_N.svg "全屏")图标获取质量得分的详细视图。

   ![](assets/brand-score-7.png)

1. 选择任意已标记的项目以查看特定反馈和AI生成的改进建议。 得分基于以下类别：

   &#x200B;* **[!UICONTROL CTA效果]**：评估您的call-to-action在多大程度上促使读者采取所需的操作。
   &#x200B;* **[!UICONTROL 主题行]**：评估清晰度、相关性和吸引注意力的质量，以鼓励打开电子邮件。
   &#x200B;* **[!UICONTROL 可读性]**：衡量内容对读者来说有多么容易理解和引人入胜。
   &#x200B;* **[!UICONTROL 垃圾邮件检查]**：识别可能影响投放能力的常见垃圾邮件触发器。
   &#x200B;* **[!UICONTROL 内容一致性]**：确保您的内容流畅处理并停留在主题上。
   &#x200B;* **[!UICONTROL 校对]**：检查拼写、语法和清晰度问题。

   ![](assets/brand-score-8.png)

1. 对于标记的文本项目，查看显示在每个问题下方的AI生成的建议，然后单击&#x200B;**[!UICONTROL 应用]**&#x200B;以替换内嵌内容，或将其关闭以保留原始文本。 [了解有关应用AI生成的建议的更多信息](#apply-suggestions)。

1. 进行更改后单击&#x200B;**[!UICONTROL 重新评估分数]**&#x200B;以刷新您的质量分数。

## 应用AI生成的建议 {#apply-suggestions}

当在品牌对齐或质量评估期间标记内容时，AI Assistant会直接在反馈面板中自动生成更正或改进的替代项。 此即用即用工作流可帮助您在不离开编辑器的情况下解决违规，从而减少手动编辑工作并加快内容生产。

人工智能生成的建议可用于所有受支持的内容类型中基于文本的违规：电子邮件、短信、推送和Web。

要应用AI生成的建议：

1. 运行品牌对齐或质量评估，然后选择标记的准则或质量项目以展开其反馈面板。

1. 查看显示在标记的内容下方的AI生成的建议。

1. 单击&#x200B;**[!UICONTROL 应用]**&#x200B;以使用建议的替代项替换标记的内容。

   若要保留原始文本，请单击&#x200B;**[!UICONTROL 关闭]**。

1. 对所有剩余的已标记项目重复此操作。

1. 重新评估您的得分以确认已应用所有改进。

## 操作方法视频 {#video}

以下视频介绍如何创建和自定义您自己的品牌，以清楚地定义您在通信中的视觉和口头身份。

+++ 观看视频

>[!VIDEO](https://video.tv.adobe.com/v/3470544/?learn=on)

+++
