---
solution: Journey Optimizer
product: journey optimizer
title: 使用 Adobe Experience Platform 数据进行个性化设置（Beta 版）
description: 了解如何使用Adobe Experience Platform数据进行个性化。
badge: label="Beta 版" type="Informative"
feature: Personalization, Rules
topic: Personalization
role: Data Engineer
level: Intermediate
keywords: 表达式，编辑器
exl-id: 2fc10fdd-ca9e-46f0-94ed-2d7ea4de5baf
source-git-commit: 47ff62f7dee5974afbffdd38dfe4a3f967781e93
workflow-type: tm+mt
source-wordcount: '1044'
ht-degree: 2%

---

# 使用 Adobe Experience Platform 数据进行个性化设置{#aep-data}

>[!AVAILABILITY]
>
>此功能目前作为公共测试版向所有客户提供。
>
>为了使用此功能，您必须首先接受贵组织的测试版条款，在个性化编辑器中添加新的“datasetLookup”帮助程序函数时会显示这些条款。

Journey Optimizer允许您在个性化编辑器中利用Adobe Experience Platform中的数据来[个性化您的内容](../personalization/personalize.md)。 为此，必须首先通过API调用启用查找个性化所需的数据集，如下所述。 完成后，可以使用其数据对您的内容进行个性化并将它们引入到 [!DNL Journey Optimizer] 中。

## Beta限制和准则 {#guidelines}

在开始之前，请查看以下限制和准则：

### 数据集启用 {#enablement}

* **数据集大小**&#x200B;在生产数据集上限制为5 GB，在开发沙盒数据集中限制为1 GB
* **在任何时候，每个组织最多可以启用50个数据集**&#x200B;以进行查找。
* **记录数**&#x200B;在生产数据集中限制为5M，在开发沙盒数据集中限制为1M。
* **数据使用标签和强制执行**&#x200B;目前未对启用查找的数据集强制执行。
* **启用查找并用于个性化设置的数据集不受删除保护**。 至于将哪些数据集用于个性化，将由您自行跟踪，以确保不会删除或删除这些数据集。

### 使用[!DNL Adobe Experience Platform]数据的Personalization {#perso}

* **支持的渠道**：目前，此功能仅可用于电子邮件、短信和直邮渠道中。
* **数据使用标签和强制执行**&#x200B;目前未对启用查找的数据集强制执行。
* **片段**：此时不能将数据集查找个性化放置在表达式或可视化片段中。

## 启用数据集进行数据查找 {#enable}

为了利用来自数据集的数据进行个性化，您需要使用API调用检索其状态并启用查找服务。

### 先决条件 {#prerequisites-enable}

* 按照[本文档](https://developer.adobe.com/journey-optimizer-apis/references/authentication/)中详述的说明配置环境以发送API命令。
* 开发人员项目必须将Adobe Journey Optimizer和Adobe Experience Platform API添加到其项目中。

  ![](assets/aep-data-api.png)

* 作为您的角色的一部分，您必须具有管理数据集权限。
* 数据集所基于的架构必须包含可用作查找键的&#x200B;**主标识**。

### API调用结构 {#call}

```
curl -s -XPATCH "https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}" \ -H "Authorization: Bearer ${ACCESS_TOKEN}" \ -H "x-api-key: ${API_KEY}" \ -H "x-gw-ims-org-id: ${IMS_ORG}" \ -H "x-sandbox-name: ${SANDBOX_NAME}"
```

其中：

* **URL**&#x200B;是`https://platform.adobe.io/data/core/entity/lookup/dataSets/${DATASET_ID}/${ACTION}`
* **数据集ID**&#x200B;是您希望启用的数据集。
* **操作**&#x200B;被启用或禁用。
* 可以从开发人员控制台检索&#x200B;**访问令牌**。
* 可从开发人员控制台检索&#x200B;**API密钥**。
* **IMS组织ID**&#x200B;是您的Adobe组织。
* **沙盒名称**&#x200B;是数据集所在的沙盒名称（即prod、dev等）。

>[!NOTE]
>
>如果在尝试通过API调用启用数据集时遇到以下错误，请尝试从开发人员控制台项目中移除Adobe Journey Optimizer API，然后重新添加它们。
>
>```
>
>"error_code": "403003", 
>"message": "Api Key is invalid"
>
>```

## 利用数据集进行个性化 {#leverage}

使用API调用为数据集启用查找个性化后，您可以使用其数据将您的内容个性化到[!DNL Journey Optimizer]中。

1. 打开个性化编辑器，您可以在每个上下文中定义个性化设置（如消息）时使用该编辑器。 [了解如何使用个性化编辑器](../personalization/personalization-build-expressions.md)

1. 导航到帮助程序函数列表，并将&#x200B;**datasetLookup**&#x200B;帮助程序函数添加到代码窗格。

   ![](assets/aep-data-helper.png)

1. 此函数提供了一个预定义语法，允许您从Adobe Experience Platform数据集调用字段。 语法如下：

   ```
   {{datasetLookup datasetId="datasetId" id="key" result="store" required=false}}
   ```

   * **datasetId**&#x200B;是您正在处理的数据集的ID。
   * **id**&#x200B;是源列的ID，它应该与查找数据集的主标识联接。

     >[!NOTE]
     >
     >为此字段输入的值可以是字段ID (*profile.packages.packageSKU*)、在历程事件中传递的字段(*context.journey.events.event_ID.productSKU*)，也可以是静态值(*sku007653*)。 无论如何，系统都将使用值，并在数据集中查找，以检查它是否与键匹配。
     >
     >如果为键使用文本字符串值，请将文本放在引号中。 例如： `{{datasetLookup datasetId="datasetId" id="SKU1234" result="store" required=false}}`。 如果将属性值用作动态键，请删除引号。 例如： `{{datasetLookup datasetId="datasetId" id=category.product.SKU result="SKU" required=false}}`

   * **结果**&#x200B;是一个任意名称，您需要提供它以引用要从数据集中检索的所有字段值。 此值将在您的代码中用于调用每个字段。

   * **required=false**：如果required设置为TRUE，则仅当找到匹配的键时，才会传递消息。 如果设置为false，则不需要匹配的密钥，并且消息仍可以投放。 请注意，如果设置为false，建议您在消息内容中考虑回退值或默认值。

   +++在哪里检索数据集ID？

   可在Adobe Experience Platform用户界面中检索数据集ID。 在[Adobe Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/catalog/datasets/user-guide#view-datasets){target="_blank"}中了解如何使用数据集。

   ![](assets/aep-data-dataset.png)

   +++

1. 调整语法以符合您的需求。 在本例中，我们要检索与乘客航班相关的数据。 语法如下：

   ```
   {{datasetLookup datasetId="1234567890abcdtId" id=profile.upcomingFlightId result="flight"}}
   ```

   * 我们正在处理ID为“1234567890abcdtId”的数据集，
   * 我们要用于与查找数据集进行联结的字段是&#x200B;*profile.exputingFlightId*，
   * 我们希望在“flight”引用下包含所有字段值。

1. 配置要在Adobe Experience Platform数据集中调用的语法后，您可以指定要检索的字段。 语法如下：

   ```
   {{result.fieldId}}
   ```

   >[!NOTE]
   >
   >在引用数据集字段时，请确保与架构中定义的完整字段路径匹配。

   * **result**&#x200B;是您分配给&#x200B;**MultiEntity**&#x200B;帮助程序函数中的&#x200B;**result**&#x200B;参数的值。 在本例中，为“flight”。
   * **fieldID**&#x200B;是要检索的字段的ID。 在浏览与数据集相关的记录架构时，此ID在[!DNL Adobe Experience Platform]用户界面中可见：

     +++从何处检索字段ID？

     在Adobe Experience Platform用户界面中预览数据集时，可以检索字段ID。 在[Adobe Experience Platform文档](https://experienceleague.adobe.com/zh-hans/docs/experience-platform/catalog/datasets/user-guide#preview){target="_blank"}中了解如何预览数据集。

     ![](assets/aep-data-field.png)

     +++

   在本例中，我们希望使用与乘客登机时间和登机口相关的信息。 因此，我们添加了这两行：

   * `{{flight._myorg.booking.boardingTime}}`
   * `{{flight._myorg.booking.gate}}`

1. 现在，您的代码已准备就绪，您可以照常完成内容，并使用&#x200B;**模拟内容**&#x200B;按钮进行测试以检查个性化。 [了解如何预览和测试内容](../content-management/preview-test.md)


   ![](assets/aep-data-sample.png)
