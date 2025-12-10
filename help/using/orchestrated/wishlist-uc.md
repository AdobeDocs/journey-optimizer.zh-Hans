---
solution: Journey Optimizer
product: journey optimizer
title: 发送愿望清单项目更新
description: 发送愿望清单项目更新
version: Campaign Orchestration
source-git-commit: 51c8c9282cb6eb9cdbd310d8f263d7973f28bbf0
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---

# 发送愿望清单项目更新 {#wishist-uc}

>[!BEGINSHADEBOX]

虽然此示例使用&#x200B;**Wishlist**&#x200B;架构，但相同的方法适用于与&#x200B;**收件人**&#x200B;具有一对多关系的任何实体，例如&#x200B;**购买**、**订阅**，或者每个收件人可能具有多个关联记录的任何自定义架构。

此用例需要&#x200B;**架构：**

* **收件人**：用作定向维度
* **WishlistItems**：包含字段： `creationDate`、`product`、`Wishlistid`
* **产品**：包含字段： `description`、`priceref`、`imageurl`
* **放弃的购物车**（可选）：带有字段： `lastmodified`

➡️ [了解如何配置基于模型的架构](gs-schemas.md)

>[!ENDSHADEBOX]

![](assets/uc-reengagement-11.png){zoomable="yes"}

这个精心设计的活动侧重于通过提醒访客保存在愿望清单中的产品来重新吸引访客。 使用Campaign Orchestration，根据愿望清单活动定义受众的条件，帮助推动访客回头转化。

1. 首先，创建一个专门针对愿望清单成员重新参与的新营销活动。 这有助于将消息传递的重点放在通过保存项目而显示购买意图的客户上。

   ![](assets/uc-reengagement-1.png){zoomable="yes"}

1. 填写您的&#x200B;**Campaign设置**。

1. 添加&#x200B;**[!UICONTROL 构建受众]**&#x200B;活动，以根据愿望清单行为识别要定位的客户组。

   ![](assets/uc-reengagement-2.png){zoomable="yes"}

1. 为此受众设置描述性&#x200B;**[!UICONTROL 标签]**，并选择&#x200B;**[!UICONTROL 收件人]**&#x200B;作为&#x200B;**[!UICONTROL 定向维度]**。 然后单击&#x200B;**[!UICONTROL 继续]**&#x200B;配置受众。

1. 单击&#x200B;**[!UICONTROL 添加条件]**&#x200B;可通过创建以下条件来优化受众：

   `WishlistItems Exist such as (creationDate greater than or equal to 36 months ago) AND (product is not empty`
或者
   `AbandonedCarts Exist such as lastmodified greater than or equal to 36 months ago`

   此受众基于这样的收件人：具有愿望清单、包含具有产品图像的项目，或者在定义的时间范围内具有放弃的购物车。

   ![](assets/uc-reengagement-3.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 计算]**&#x200B;可查看受这些条件影响的配置文件数，单击&#x200B;**[!UICONTROL 查看结果]**&#x200B;可检查每个条件的详细信息并确认受众与目标区段匹配。

   ![](assets/uc-reengagement-4.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 确认]**。

1. 添加&#x200B;**[!UICONTROL 扩充]**&#x200B;活动以使用&#x200B;**愿望清单**&#x200B;和&#x200B;**产品信息**&#x200B;个性化营销活动。

   ![](assets/uc-reengagement-5.png){zoomable="yes"}

1. 单击&#x200B;**[!UICONTROL 添加扩充数据]**。

1. 访问`Targeting dimension > Wishlistitems > Wishlistid`。

   ![](assets/uc-reengagement-6.png){zoomable="yes"}

1. 选择收集数据的方式，在这种情况下，**[!UICONTROL 收集数据]**&#x200B;以收集受众的愿望清单详细信息。

1. 选择要检索的行数。 默认情况下，每个愿望清单会检索三个项目，但可以根据促销活动需要突出显示更多或更少产品，进行调整。

1. 单击&#x200B;**[!UICONTROL 添加属性]**&#x200B;以创建以下三个属性：

   * `Product > description`
   * `Product > priceref`
   * `Product > imageurl`

   这将通过详细的产品信息丰富消息，以提高转化率。

   ![](assets/uc-reengagement-7.png){zoomable="yes"}

1. 添加电子邮件活动，为每个客户创建个性化的重新参与消息。 单击&#x200B;**[!UICONTROL 编辑内容]**&#x200B;开始设计内容。

   ➡️ [了解有关电子邮件个性化的更多信息](../email/content-from-scratch.md)

   ![](assets/uc-reengagement-8.png){zoomable="yes"}

1. 完成电子邮件后，单击编排的营销活动中的&#x200B;**[!UICONTROL 开始]**，以草稿模式保存并运行营销活动。

1. 启动草稿模式后，使用愿望清单详细信息预览受众。

   要获得更深入的见解，请单击输出结果，然后选择&#x200B;**[!UICONTROL 预览结果]**。

   ![](assets/uc-reengagement-10.png){zoomable="yes"}

营销活动运行后，我们可以探索报表，这些报表会为我们提供一组关于营销活动表现的强大数据和KPI。

➡️ [了解有关报告的更多信息](../reports/campaign-global-report-cja.md)
