---
title: 创建排名公式
description: 了解如何在Adobe Experience Platform中创建排名公式。
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 3%

---

# 创建排名公式 {#create-ranking-formulas}

## 关于排名公式{#about-ranking-formulas}

**排** 名公式允许您定义规则，这些规则将确定在给定位置应首先显示哪些优惠，而不是考虑优惠的优先级得分。

排名公式以&#x200B;**PQL语法**&#x200B;表示，并可利用用户档案属性、上下文数据和优惠属性。 有关如何使用PQL语法的详细信息，请参阅[专用文档](https://experienceleague.adobe.com/docs/experience-platform/segmentation/pql/overview.html)。

一旦创建了排名公式，您就可以将其分配给决策中的位置(以前称为优惠活动)。 有关详细信息，请参阅[在决策](../offer-activities/configure-offer-selection.md)中配置优惠选择。

## 创建排名公式{#create-ranking-formula}

要创建排名公式，请执行以下步骤：

* 访问&#x200B;**[!UICONTROL Components]**&#x200B;菜单，然后选择&#x200B;**[!UICONTROL Rankings]**&#x200B;选项卡。

* 单击&#x200B;**[!UICONTROL Create formula]**&#x200B;可创建新的排名公式。

   ![](../../assets/ranking-create-formula.png)

* 指定排名公式名称、说明和公式。

   在此示例中，我们希望在实际天气炎热时使用“hot”属性提升所有优惠的优先级。 为此，在决策调用中传递了&#x200B;**contextData.weather=hot**。

   ![](../../assets/ranking-syntax.png)

* 单击 **[!UICONTROL Save]**。您的排名公式已创建，您可以从列表中选择它以获取详细信息并编辑或删除它。

   现在，它已准备好用于对符合条件的优惠进行排名以进行放置的决定(请参阅[在决定](../offer-activities/configure-offer-selection.md)中配置优惠选择)。

   ![](../../assets/ranking-formula-created.png)
