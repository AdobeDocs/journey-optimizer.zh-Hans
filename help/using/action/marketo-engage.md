---
solution: Journey Optimizer
product: journey optimizer
title: 与 Marketo Engage 集成
description: 了解如何使用Marketo Engage操作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: marketo、marketo engage集成
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: a5ee7c668b51a761266b50216047caf48496f678
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 4%

---

# 与 Marketo Engage 集成 {#integrating-with-marketo-engage}

开始与Marketo Engage无缝数据集成的历程。 您的历程中提供了特定的自定义操作，用于集成Adobe Journey Optimizer和Marketo Engage。 此自定义操作支持摄取两种关键数据类型：

* **人员**（个人资料）： Marketo将个人资料转换为可操作洞察。
* **自定义对象**：使用自定义对象（如产品）定制您的数据，以实现个性化的营销方法。

## 先决条件 {#prerequisites}

以下先决条件适用于此集成：

* Marketo Engage的客户实例必须已启用IMS。
* Marketo Engage实例和Adobe Experience Platform/Journey Optimizer实例必须位于同一组织中。
* 必须为客户设置&#x200B;**MktoSync：摄取服务访问**

## 配置操作 {#configure-marketo-action}


在Journey Optimizer中，必须配置Marketo Engage的自定义操作。 执行以下步骤：

1. 在“管理”菜单部分中选择&#x200B;**[!UICONTROL 配置]**。
1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 创建操作]**。 操作配置窗格将在屏幕右侧打开。
1. 输入名称、描述，然后选择&#x200B;**Adobe Marketo Engage**&#x200B;作为&#x200B;**操作类型**

![](assets/engage-customaction-creation.png){width="40%" align="left"}

1. 单击&#x200B;**请求**&#x200B;和&#x200B;**响应**&#x200B;负载的&#x200B;**编辑负载**&#x200B;图标。
1. 对于这两种情况，请撰写有效负载并将其粘贴到专用弹出窗口中。

![](assets/engage-customaction-payload.png){width="70%" align="left"}

1. 检查和配置有效负载值
注意：若要动态传递值，请为每个字段将**常量**&#x200B;更改为&#x200B;**变量**。

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. 在字段配置屏幕中单击&#x200B;**保存**，然后单击&#x200B;**保存**&#x200B;您的自定义操作。

您现在可以在历程画布上使用自定义操作。

## 有效负载语法 {#payload-syntax}

### 人员

![](assets/payload-person.png)

### 自定义对象

![](assets/payload-customobject.png)


针对人员&#x200B;**的**&#x200B;有效负载示例

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

自定义对象的&#x200B;**有效负载示例**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## 使用操作 {#engage-using}

对于所配置的每个操作，旅程设计器面板中都提供Marketo Engage操作活动。

要使用它，请执行以下步骤：

1. 将自定义操作拖动到历程画布上。

1. 输入此操作的标签和说明。

1. 在&#x200B;**请求参数**&#x200B;部分中，单击每个参数的&#x200B;**编辑**&#x200B;图标，然后查看已在有效负载中配置的动态值。

![](assets/engage-use-canvas.png){width="70%" align="left"}
