---
solution: Journey Optimizer
product: journey optimizer
title: AEM内容片段
description: 了解如何管理AEM内容片段
topic: Content Management
role: User
level: Beginner
source-git-commit: ce34eb885d85c6c0f81b477e155cb81547d53e03
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 管理您的Adobe Experience Manager内容片段 {#aem-fragments}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;从内容管理片段列表管理AEM内容片段以监视状态和元数据，查看片段在历程和营销活动中的使用位置，从Experience Manager同步发布的更新，以及在不离开Journey Optimizer的情况下打开片段进行编辑。

>[!ENDSHADEBOX]

通过将Adobe Experience Manager as a Cloud Service或Managed Services与Adobe Journey Optimizer集成，您可以在内容中使用AEM内容片段，并在不离开Journey Optimizer的情况下检查片段状态。

当您重新发布历程或营销活动中已使用的片段时，同步计时器将在Adobe Experience Manager中&#x200B;**已发布**&#x200B;该片段之后启动。 对于单一历程和营销活动，更新后的内容通常会在大约&#x200B;**5分钟**&#x200B;内在Journey Optimizer中提供；对于批量投放，此更改将出现在&#x200B;**下一个处理批次**&#x200B;中。 请参阅[使用Adobe Experience Manager内容片段](aem-fragments.md)。 如果出现延迟，您可以从Journey Optimizer手动同步该片段，以提取最新发布的版本。

## 访问AEM内容片段 {#access-aem-fragments}

1. 从&#x200B;**[!UICONTROL 内容管理]**&#x200B;菜单中，选择&#x200B;**[!UICONTROL 片段]**。

1. 打开&#x200B;**[!UICONTROL AEM片段]**&#x200B;选项卡以查看Adobe Experience Manager中可用的内容片段。

1. 在片段列表中，单击![高级菜单](assets/do-not-localize/Smock_FolderSearch_18_N.svg)以&#x200B;**[!UICONTROL 浏览引用]**。

   ![](assets/fragment-list-1.png)

1. 选择片段可查看其状态和可用操作：

   * **[!UICONTROL 浏览引用]**：查看使用片段的历程、营销活动、编排的营销活动和模板。
   * **[!UICONTROL 在AEM中打开]**：在Adobe Experience Manager中打开片段进行编辑或重新发布。
   * **[!UICONTROL 同步]**：将最新发布的版本从Adobe Experience Manager提取到Journey Optimizer中，例如，当重新发布的内容未出现在常规同步窗口之后时。 如果禁用了控件，则片段已与Experience Manager中的已发布版本匹配。

     ![](assets/fragment-list-2.png)

1. **[!UICONTROL 详细信息]**&#x200B;菜单允许您查看元数据和预览同步的有效负载：

   * **[!UICONTROL 名称]**：从Adobe Experience Manager导入的内容片段的标题。
   * **[!UICONTROL 描述]**：从Adobe Experience Manager导入的描述。
   * **[!UICONTROL 变量]**：当前代表此片段的已发布变量。
   * **[!UICONTROL 存储库ID]**： Adobe Experience Manager中片段的存储库标识符。
   * **[!UICONTROL AEM片段ID]**： Adobe Experience Manager中的唯一内容片段标识符。
   * **[!UICONTROL 标记]**：在Adobe Experience Manager中分配的标记，包括Journey Optimizer启用标记，用于确定片段是否显示在您的组织和沙盒的选择器中。 [了解如何创建和分配标记](aem-fragments.md#create-tag)
   * **[!UICONTROL JSON预览]**： Journey Optimizer使用的片段内容的只读JSON结构。

1. 在&#x200B;**[!UICONTROL 浏览引用]**&#x200B;中，使用选项卡查看引用片段的历程、营销策划、编排的营销活动和模板。

   ![](assets/fragment-list-3.png)

➡️ [了解有关内容片段的更多信息](aem-fragments.md)


