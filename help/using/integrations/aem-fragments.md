---
solution: Journey Optimizer
product: journey optimizer
title: AEM内容片段
description: 了解如何访问和管理AEM内容片段
topic: Content Management
role: User
level: Beginner
exl-id: 57d7c25f-7e39-46ad-85c1-65e2c18e2686
source-git-commit: 92690f1b3f73c75d9b81746b49836a24ebf7c457
workflow-type: tm+mt
source-wordcount: '1510'
ht-degree: 4%

---

# Adobe Experience Manager 内容片段 {#aem-fragments}

通过将 Adobe Experience Manager as a Cloud Service 与 Adobe Journey Optimizer 集成，您现在可以将 AEM 内容片段无缝纳入到 Journey Optimizer 内容中。这种简单的连接方式可简化访问和利用 AEM 内容的流程，从而能够创建个性化的动态营销活动和历程。

要了解有关AEM内容片段的更多信息，请参阅Experience Manager文档中的[使用内容片段](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragments-with-journey-optimizer){target="_blank"}。

## 开始前 {#start}

>[!AVAILABILITY]
>
>对于医疗保健客户，只有在许可Journey Optimizer Healthcare Shield和Adobe Experience Manager增强安全性附加产品后，才会启用集成。

### 限制 {#limitations}

在Journey Optimizer中使用Adobe Experience Manager内容片段时，请注意以下限制：

* **内容片段类型**：支持简单内容片段和嵌套内容片段。 当前不支持内容片段变体。

* **多语言内容**：仅支持手动流。 每个语言变体都必须在Adobe Experience Manager中独立创作、在Journey Optimizer中标记、发布和手动选择。 没有自动语言解析或回退机制。

* **存储库访问**： Journey Optimizer与Adobe Experience Manager发布层独占集成，在该发布层中，内容片段可通过未经身份验证的公用端点使用。 虽然创作存储库可能显示在存储库选择器中，但Journey Optimizer中只能使用发布到发布层的内容片段。

* **内容片段状态**： Journey Optimizer显示状态为&#x200B;**已发布**&#x200B;和&#x200B;**已修改**&#x200B;的内容片段。 在所有情况下，仅使用最新发布的版本。 如果片段在发布后进行了修改，则在内容片段在Adobe Experience Manager中重新发布之前，这些更改将不会反映在Journey Optimizer中。 Adobe Experience Manager和Journey Optimizer之间没有自动版本协调。

* **Personalization**：仅支持配置文件属性、上下文属性、静态字符串和预声明的变量。 不支持派生或计算属性。

* **更新和版本控制**：内容片段更新需要从Adobe Experience Manager中手动重新发布。 Adobe Experience Manager和Journey Optimizer之间没有自动版本协调。 在Adobe Experience Manager中发布内容片段时，Journey Optimizer在Journey Optimizer端接收事件并进行更新。 如果成功，对于单一历程，更新将在5分钟后可用，对于批量用例，更新将在下一批次中可用。

* **缓存和校对**：从Adobe Experience Manager发布层实时检索内容片段。 没有预渲染或快照缓存。 营销活动和历程的验证始终反映内容片段的最新发布版本，并且无法锁定历史版本以进行验证。

* **用户访问权限**：建议限制有权发布内容片段的用户的数量，以降低意外错误的风险。

### 内容同步流程 {#content-sync-flow}

Adobe Experience Manager与Journey Optimizer之间的集成将遵循以下数据流：

1. **[创建并创作](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#creating-a-content-fragment)**：内容在Adobe Experience Manager中创建并配置为内容片段。

1. **[标记](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#manage-tags)**：内容片段必须使用特定于Journey Optimizer的标记(`ajo-enabled:{OrgId}/{SandboxName}`)进行标记。

1. **[发布](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing#publishing-and-previewing-a-fragment)**：内容片段已在Adobe Experience Manager中发布，可用于Journey Optimizer。

1. **[访问](#aem-add)**： Journey Optimizer从Adobe Experience Manager发布实例实时获取并显示可用的内容片段。

1. **[集成](#aem-add)**：已选择内容片段并将其集成到营销活动或历程中。

在Adobe Experience Manager中发布内容片段时，将发送一个事件以更新Journey Optimizer端的内容。 如果更新成功，内容片段将在大约5分钟内可用于单一历程，并在下一个处理批次中可用于批量用例。 在Journey Optimizer中提供更新后，将在所有适用的营销活动和历程中使用最新发布的内容。

### 内容片段生命周期

![](assets/do-not-localize/AEM_CF.png)

内容片段根据它们所在的Adobe Experience Manager层而遵循不同的生命周期阶段。 [请参阅Adobe Experience Manager文档以了解详情](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/authoring/author-publish)

内容在&#x200B;**创作层**&#x200B;中创建和管理，其中片段可以具有状态，如“新建”、“草稿”、“已发布”、“已修改”或“未发布”。 这些状态仅适用于&#x200B;**创作层**，并且支持内容创建和审阅。

发布内容片段时，会在&#x200B;**发布层**&#x200B;上创建一个副本，并通过未经身份验证的公共端点公开。 Journey Optimizer与此&#x200B;**发布层**&#x200B;独占集成。

因此，Journey Optimizer只会显示已发布或已修改的内容片段，并且始终使用最新发布的版本。 在重新发布内容片段之前，发布后所做的任何更改都不会反映在Journey Optimizer中。

## 在Experience Manager中创建并分配标记

在Journey Optimizer中使用内容片段之前，您需要创建专门用于Journey Optimizer的标记：

1. 访问您的&#x200B;**Experience Manager**&#x200B;环境。

1. 从&#x200B;**工具**&#x200B;菜单中选择&#x200B;**标记**。

   ![](assets/do-not-localize/aem_tag_1.png)

1. 单击&#x200B;**创建标记**。

1. 确保ID遵循以下语法： `ajo-enabled:{AJO-OrgId}/{AJO-SandboxName}`。

1. 单击&#x200B;**创建**。

1. 按照[Experience Manager文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/content-fragment-models){target="_blank"}中的详细说明定义您的内容片段模型，并分配新创建的Journey Optimizer标记。

这种实时连接可确保您的内容始终保持最新，但也意味着对已发布片段的任何更改都将立即影响活动的营销活动和历程。

您现在可以开始创建和配置内容片段，以供将来在Journey Optimizer中使用。 请参阅[Experience Manager文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/managing){target="_blank"}以了解详情。

## 添加Experience Manager内容片段 {#aem-add}

创建并个性化您的AEM内容片段后，您现在可以将其导入您的历程优化器促销活动或历程。

1. 创建您的[促销活动](../campaigns/create-campaign.md)或[历程](../building-journeys/journey-gs.md)。

1. 要访问AEM内容片段，请单击任意文本字段中的![Personalization图标](assets/do-not-localize/Smock_PersonalizationField_18_N.svg)，或通过HTML内容组件打开源代码。

   ![](assets/aem_campaign_2.png)

1. 从左窗格中的&#x200B;**[!UICONTROL AEM内容片段]**&#x200B;菜单中，单击&#x200B;**[!UICONTROL 打开AEM CF选择器]**。

   ![](assets/aem_campaign_3.png)

1. 从可用列表中选择一个&#x200B;**[!UICONTROL 内容片段]**&#x200B;以导入到您的Journey Optimizer内容中。

1. 单击&#x200B;**[!UICONTROL 显示筛选器]**&#x200B;以优化您的内容片段列表。

   默认情况下，内容片段过滤器预设为仅显示批准的内容。

   ![](assets/aem_campaign_4.png)

1. 选择您的&#x200B;**[!UICONTROL 内容片段]**&#x200B;后，单击&#x200B;**[!UICONTROL 选择]**&#x200B;以将其打开。

   ![](assets/aem_campaign_5.png)

1. 单击&#x200B;**[!UICONTROL 查看片段]**&#x200B;以显示您的片段信息。 请注意，打开&#x200B;**[!UICONTROL 片段信息]**&#x200B;菜单会将编辑器置于只读模式。

   从右侧菜单中选择&#x200B;**[!UICONTROL 预览]**&#x200B;可在Adobe Experience Manager中查看您的片段。

   ![](assets/aem_campaign_7.png)

1. 单击![更多操作图标](assets/do-not-localize/Smock_MoreSmallList_18_N.svg)访问片段的高级菜单：

   * **[!UICONTROL 交换片段]**
   * **[!UICONTROL 浏览引用]**
   * 在AEM中&#x200B;**[!UICONTROL 打开]**

   ![](assets/aem_campaign_8.png)

1. 从&#x200B;**[!UICONTROL 片段]**&#x200B;中选择要添加到内容的所需字段。
   <!--
    Note that if you choose to copy the value, any future updates to the Content Fragment will not be reflected in your campaign or journey. However, using dynamic placeholders ensures real-time updates.-->

   ![](assets/aem_campaign_6.png)

1. 要启用实时个性化，用户必须将&#x200B;**[!UICONTROL 内容片段]**&#x200B;中使用的所有占位符显式声明为片段帮助程序标记中的参数。 可以使用以下方法将这些占位符映射到配置文件属性、上下文属性、静态字符串或预定义变量：

   1. **配置文件或上下文属性映射**：将占位符分配给配置文件或上下文属性，例如name = profile.person.name.firstName。

   1. **静态字符串映射**：通过将其置于双引号中来分配固定字符串值，例如name = &quot;John&quot;。

   1. **变量映射**：引用之前在同一HTML中声明的变量，例如name = &#39;variableName&#39;。
在这种情况下，请确保在添加片段ID之前使用以下语法声明&#x200B;**_variableName_**：

      ```html
      {% let variableName = attribute name %} 
      ```

   在以下示例中，**_name_**&#x200B;占位符映射到片段中的&#x200B;**_profile.person.name.firstName_**&#x200B;属性。

   ![](assets/aem_campaign_9.png){zoomable="yes"}

1. 单击 **[!UICONTROL Save]**。您现在可以测试和检查您的邮件内容，如[此部分](../content-management/preview.md)中所详述。
执行测试并验证内容后，您可以[发送营销活动](../campaigns/review-activate-campaign.md)或[将您的历程](../building-journeys/publish-journey.md)发布给受众。

Adobe Experience Manager允许您识别正在使用内容片段的Journey Optimizer营销活动或历程。 请参阅[Adobe Experience Manager文档](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/sites/administering/content-fragments/extension-content-fragment-ajo-external-references)以了解详情。

## 故障排除 {#troubleshooting}

如果您在Journey Optimizer中使用Adobe Experience Manager内容片段时遇到问题，请参阅以下常见问题和解决方案：

| 问题 | 原因 | 解决方法 |
|-|-|-|
| **标记未找到**&#x200B;或&#x200B;**内容片段在选择器中不可见** | Adobe Experience Manager标记语法与必需的格式`ajo-enabled:{OrgId}/{SandboxName}`不匹配 | 验证标记ID是否使用正确的&#x200B;**组织ID**&#x200B;和&#x200B;**沙盒名称**。 确保没有空格或分隔符不正确。 更正标记后重新发布内容片段。 |
| **内容片段未出现在列表**&#x200B;中 | 内容片段处于草稿状态或未批准 | Journey Optimizer选择器中仅显示已批准和已发布的内容片段。 在Adobe Experience Manager中发布内容片段并确保其状态为已批准。 |
| **变量未定义错误** | 未在片段帮助程序标记中声明Personalization占位符 | 在片段帮助程序标记中添加所有必需的参数。 内容片段中使用的每个占位符必须使用其映射进行显式声明。 |
| **校对显示意外内容** | 校对使用Adobe Experience Manager中最新发布的版本 | 验证始终反映Adobe Experience Manager中内容片段的最新发布。 如果您最近在Adobe Experience Manager中进行了更改，请重新发布片段并刷新验证。 |
| **访问被拒绝(CPES)错误** | 用户角色无权访问某些属性 | 请联系您的系统管理员，以验证您的角色是否对个性化中使用的配置文件或上下文属性具有适当的权限。 |
| **片段显示空白或缺少内容** | 缺少所需的个性化参数或回退值 | 请确保提供了所有必需的参数，并考虑为可选属性添加回退值。 |

如果问题仍然存在，请与Adobe代表联系，告知有关内容片段ID、营销活动或历程ID的详细信息，以及显示的任何错误消息。
