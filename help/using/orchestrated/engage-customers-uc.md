---
solution: Journey Optimizer
product: journey optimizer
title: 通过浏览活动吸引客户
description: 通过浏览活动吸引客户
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '569'
ht-degree: 2%

---

# 通过浏览活动吸引客户 {#engage-customers-uc}

>[!BEGINSHADEBOX]

请注意，此用例首先是Experience Platform中已存在的受众，特别是实时网络行为受众，该受众在浏览活动发生时收集浏览活动。 [在Adobe Experience Platform中了解详情](https://experienceleague.adobe.com/en/docs/experience-platform/rtcdp/intro/rtcdp-intro/get-started#audiences)

此用例需要&#x200B;**架构：**

* **收件人**：用作定向维度，字段： `email`，`churnprop`
* **愿望清单**：包含字段： `description`、`priceref`、`imageurl`

➡️ [了解如何配置基于模型的架构](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-interest-14.png){zoomable="yes"}

此营销活动面向浏览练习设备类别的客户。 根据客户流失风险（即某人停止接触或购买的可能性），为受众去除了重复项，并做了分段。

高风险客户会聚集到单独的新受众中，这些受众稍后将用于特定通信，而低风险和中风险客户则通过个性化的电子邮件和跟进经历多步历程。

1. 首先设置专门针对&#x200B;**愿望清单重新参与**&#x200B;的新营销活动。 这可确保您的消息聚焦于已通过将产品保存到愿望清单而显示购买意图的客户。

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. 填写您的&#x200B;**[!UICONTROL 促销活动设置]**，如促销活动名称、描述、开始和结束日期以及相关标记。

1. 添加&#x200B;**[!UICONTROL 读取受众]**&#x200B;活动以从Adobe Experience Platform中选择预定义的受众，此处为已在您的网站上浏览过该健身设备类别的客户。

   收件人的电子邮件地址是从&#x200B;**[!UICONTROL 实体]**&#x200B;字段中选择的。

   ![](assets/uc-interest-1.png){zoomable="yes"}

1. 添加&#x200B;**[!UICONTROL 重复数据删除]**&#x200B;活动，以从受众中删除重复的电子邮件地址，确保每个客户仅收到一封邮件。

1. 单击&#x200B;**[!UICONTROL 添加属性]**&#x200B;并选择电子邮件作为重复数据删除的属性。

   ![](assets/uc-interest-2.png){zoomable="yes"}

1. 接下来，添加&#x200B;**[!UICONTROL 拆分]**&#x200B;活动以根据客户流失的可能性对客户进行分段，从而允许您针对每个客户组提供量身定制的个性化体验。

   ![](assets/uc-interest-3.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加区段]**&#x200B;以创建三个组：

   * 低风险

   * Medium风险

   * 高风险

   ![](assets/uc-interest-5.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 创建过滤器]**&#x200B;以定义每个组的流失概率。

   使用&#x200B;**条件编辑器**&#x200B;设置用于确定每个客户的客户流失风险的特定值。

   ![](assets/uc-interest-6.png){zoomable="yes"}

1. 每个区段的处理方式不同：

   * [低/中风险](#low-medium-risk)
   * [高风险](#high-risk)

1. 营销活动测试完成并准备就绪后，单击&#x200B;**[!UICONTROL 发布]**&#x200B;即可使其上线。

活动运行后，浏览报表仪表板以查看绩效指标和关键见解。

➡️ [了解有关报告的更多信息](../reports/campaign-global-report-cja.md)

## 高风险区段 {#high-risk}

对于被识别为具有高流失风险的客户，请创建专用的受众区段。 此受众稍后用于单独的、有针对性的通信。

1. 添加&#x200B;**[!UICONTROL 保存受众]**。

   ![](assets/uc-interest-7.png){zoomable="yes"}

1. 向受众添加&#x200B;**[!UICONTROL 标签]**，然后选择&#x200B;**[!UICONTROL 配置文件映射字段]**，此处为&#x200B;**收件人 — 电子邮件**。

   ![](assets/uc-interest-8.png){zoomable="yes"}

然后，此受众将保存到Experience Cloud，以便稍后用于特定的定向营销活动。

## 低/中风险区段 {#low-medium-risk}

对于流失风险处于中低位的客户，应设置一个多步式营销活动，旨在加强参与：

1. 将低风险和Medium风险与&#x200B;**[!UICONTROL 合并]**&#x200B;活动相结合。

   ![](assets/uc-interest-9.png){zoomable="yes"}

1. 添加&#x200B;**[!UICONTROL 扩充]**&#x200B;活动以使用愿望清单和产品信息个性化营销活动。

1. 单击&#x200B;**[!UICONTROL 添加属性]**&#x200B;以创建以下三个属性：

   * `Wishlist > description`
   * `Wishlist > priceref`
   * `Wishlist > imageurl`

   这用详细的愿望清单信息丰富了消息。

   ![](assets/uc-interest-10.png){zoomable="yes"}

1. 根据与电子邮件的交互情况，创建新的受众以重新定位。

   在此处，我们根据电子邮件点击事件创建一个受众，以重新定位与之前发送的电子邮件交互的所有人员，更具体地说，就是单击该邮件中的链接的所有人员。

   ![](assets/uc-interest-11.png){zoomable="yes"}

1. 平均分配参与以通过短信或推送通知发送跟进来鼓励转化。

   ![](assets/uc-interest-12.png){zoomable="yes"}

1. 为每个渠道创建消息内容（包括用户档案属性，如收件人的姓名）以及愿望清单项目等扩充数据，以个性化每条消息。

   ![](assets/uc-interest-13.png){zoomable="yes"}
