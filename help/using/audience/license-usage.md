---
solution: Journey Optimizer
product: journey optimizer
title: 许可证用量仪表板
description: 了解Journey Optimizer许可证使用情况仪表板
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 7e91face-c8f4-4e70-9123-9e36bae7e67e
source-git-commit: db1e4ee5b2b4bb3a3d7d9e86aded14ad3c613765
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---

# 许可证用量仪表板 {#license-usage}

[!DNL Adobe Journey Optimizer] [用户界面](../start/user-interface.md)提供了一个仪表板，该仪表板显示有关您组织的许可证使用情况的重要信息，这些信息是在每日快照期间捕获的。

若要访问此仪表板，请转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 许可证使用情况]**。 这将打开&#x200B;**[!UICONTROL 概述]**&#x200B;选项卡，其中显示仪表板。

![许可证使用情况仪表板概述](assets/license-usage-dashboard.png)

>[!NOTE]
>
>* 要查看仪表板，您必须具有[查看许可证使用情况仪表板](https://experienceleague.adobe.com/docs/experience-platform/dashboards/permissions.html?lang=zh-Hans#available-permissions){target="_blank"}权限。
>
>* 某些量度（例如，计算小时数、电子邮件）不显示为开发沙盒，如配额列中的`N/A`所指示。 仪表板中仅显示非空值：当指标为零或接近零时，不填充这些指标。


对于[!DNL Adobe Journey Optimizer]，仪表板允许您检查&#x200B;**可启用的用户档案**&#x200B;的数量。

## 什么是可参与配置文件？ {#what-is-engageable-profile}

**可参与的配置文件**&#x200B;是代表个人信息的记录，该信息存储在配置文件服务中并且已由历程或营销活动参与。

可参与用户档案的关键特征：

* **12个月的滚动时段**：可参与的用户档案是根据过去12个月的参与度计算的。 此量度显示您尝试使用Journey Optimizer的创作、决策、交付、试验或编排功能与之互动的独特用户档案的数量。

* 每个沙盒的&#x200B;**唯一计数**：如果配置文件在沙盒内进入多个历程或营销活动，则它仅作为该沙盒的单个可参与配置文件计数一次。

* **基于可寻址受众**：可预订配置文件是根据您的可寻址受众计算的。 该计数表示过去12个月内使用Journey Optimizer的任意功能参与的受众（在可寻址受众总数中）。

* **量度行为**：可参与的配置文件计数：
   * 当新用户档案通过历程或营销活动参与时，可能会增加
   * 除非与某些用户档案已有12个月以上未互动，否则无法减少
   * 将假名配置文件拼合到已知配置文件时，可能会减少

>[!NOTE]
>
>如果您发现可参与用户档案计数突然激增，请参阅下面的[故障排除部分](#troubleshooting-engageable-profiles)，了解有关了解和解决此问题的详细指导。

## 故障排除：可参与用户档案计数显着增加 {#troubleshooting-engageable-profiles}

如果您发现可参与用户档案计数突然激增（例如，用户档案在一天内从数十万增加到数百万），本节将提供有关如何理解和解决此问题的指导。

### 了解增长

可参与用户档案量度反映过去12个月历程或营销活动所参与的独特用户档案数。 突然增加可能是由于：

* 新历程或营销活动所定向的大型受众
* 为配置文件服务启用的数据集的更改
* 批量处理最近未参与的受众

### 解决步骤

要解决此问题，请执行以下步骤：

1. **了解配置文件计数逻辑：**

   * 可参与用户档案是根据过去12个月中历程或营销活动参与的唯一用户档案计算的。
   * 如果配置文件进入多个历程，则被计为该沙盒的一个可参与配置文件。
   * 除非已超过12个月没有与某些用户档案互动，或者匿名用户档案已拼合到已知用户档案，否则量度无法降低。
   * 可参与用户档案使用客户的可寻址受众进行计算。
   * 过去12个月内使用Journey Optimizer的任何功能参与的受众在可寻址受众总数中决定了可参与用户档案的数量。

2. **调查针对大型受众的历程、营销活动和决策：**

   * 使用[可启用的用户档案查询](../reports/query-examples.md#engageable-profiles-queries)或[查询服务](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/query/home){target="_blank"}查看最近针对大量用户档案的历程和营销活动。
   * 识别导致用户档案计数激增的特定历程版本。
   * 涉及新配置文件的历程、营销活动和决策可能会导致历程数据集中的事件计数增加，从而导致可参与配置文件计数增加。

3. **在历程和营销活动级别筛选受众：**

   * 在启动历程或营销活动之前，在受众级别应用过滤器，以防止可参与用户档案不必要的增加。
   * 确保在参与期间仅定向相关受众。

4. **减少可寻址受众大小：**

   * 根据需要删除假名配置文件。 请注意，此操作会同时影响Journey Optimizer和Real-Time Customer Data Platform。
   * 在实时客户个人资料指南中了解有关[假名个人资料数据过期](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/profile/pseudonymous-profiles){target="_blank"}的更多信息。
   * **注意：**&#x200B;无法通过Platform UI或API配置假名配置文件数据过期。 要启用此功能，必须联系支持人员。

5. **监视数据集更改：**

   * 验证为分析启用的数据集，并确保它们不包含过多的ECID (Experience Cloud ID)。
   * 如果需要，请删除具有高ECID计数的数据集，然后使用较少的记录重新创建它们。

6. **制定长期缩减策略：**

   * 如果某些用户档案未使用超过12个月，可使用的用户档案计数将自然减少。

**另请参阅：**

* [可参与用户档案查询示例](../reports/query-examples.md#engageable-profiles-queries) — 用于监视和分析可参与用户档案的示例查询
* [Adobe Experience Platform查询服务概述](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/query/home){target="_blank"}

## 相关文档 {#related-documentation}

请参阅Adobe Experience Platform文档以了解详情：

* [许可证使用情况仪表板概述](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hans){target="_blank"}
* [浏览许可证使用情况仪表板](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hans#exploring-the-license-usage-dashboard){target="_blank"}
* [可用量度](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/license-usage.html?lang=zh-Hans#%E5%8F%AF%E7%94%A8%E9%87%8F%E5%BA%A6){target="_blank"}
* [假名配置文件数据过期](https://experienceleague.adobe.com/docs/experience-platform/profile/pseudonymous-profiles.html?lang=zh-Hans){target="_blank"}
