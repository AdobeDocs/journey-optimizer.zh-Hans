---
solution: Journey Optimizer
product: journey optimizer
title: 创建测试轮廓
description: 了解如何创建测试用户档案
feature: Profiles, Test Profiles
topic: Content Management
role: User
level: Intermediate
exl-id: bd5e053a-69eb-463b-add3-8b9168c8e280
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '1351'
ht-degree: 3%

---

# 创建测试轮廓 {#create-test-profiles}

在历程中使用[测试模式](../building-journeys/testing-the-journey.md)时需要测试配置文件，并且需要[预览和测试您的内容](../content-management/preview-test.md)。


>[!NOTE]
>
>[!DNL Journey optimizer]允许测试内容的不同变体，方法是预览内容并使用从CSV或JSON文件上传或手动添加的示例输入数据发送校样。 [了解如何使用示例输入数据测试内容](../test-approve/simulate-sample-input.md)

可通过多种方式创建测试用户档案。 您可以在此页面中查找以下详细信息：

* 将[现有配置文件](#turning-profile-into-test)转换为测试配置文件

* 通过上传[CSV文件](#create-test-profiles-csv)或使用[API调用](#create-test-profiles-api)创建测试配置文件。

  Adobe Journey Optimizer还提供了一个特定的[产品内用例](#use-case-1)，以便于创建测试配置文件。

您可以将JSON文件上传到现有数据集。 有关详细信息，请参阅[数据摄取文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=zh-Hans#add-data-to-dataset){target="_blank"}。

请注意，创建测试用户档案与在Adobe Experience Platform中创建常规用户档案类似。 有关详细信息，请参阅[实时客户资料文档](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}。

➡️ [在此视频中了解如何创建测试配置文件](#video)

## 先决条件 {#test-profile-prerequisites}

要创建配置文件，您首先需要在Adobe [!DNL Journey Optimizer]中创建架构和数据集。

### 创建架构

要&#x200B;**创建架构**，请执行以下步骤：

1. 在“数据管理”菜单部分中，单击&#x200B;**[!UICONTROL 架构]**。
   ![](assets/test-profiles-0.png)
1. 单击&#x200B;**[!UICONTROL 创建架构]**，在右上角选择架构类型，例如&#x200B;**个人资料**，然后单击&#x200B;**下一步**。
   ![](assets/test-profiles-1.png)
1. 输入架构的名称，然后单击&#x200B;**完成**。
   ![](assets/test-profiles-1-bis.png)
1. 在&#x200B;**字段组**&#x200B;部分的左侧，单击&#x200B;**添加**&#x200B;并选择适当的字段组。 确保添加&#x200B;**配置文件测试详细信息**&#x200B;字段组。
   ![](assets/test-profiles-1-ter.png)
完成后，单击&#x200B;**[!UICONTROL 添加字段组]**：字段组的列表将显示在架构概述屏幕上。
   ![](assets/test-profiles-2.png)

   >[!NOTE]
   >
   >单击架构的名称可更新其属性。

1. 在字段列表中，单击要定义为主标识的字段。
   ![](assets/test-profiles-3.png)
1. 在&#x200B;**[!UICONTROL 字段属性]**&#x200B;右侧窗格中，检查&#x200B;**[!UICONTROL 标识]**&#x200B;和&#x200B;**[!UICONTROL 主标识]**&#x200B;选项并选择命名空间。 如果希望主标识是电子邮件地址，请选择&#x200B;**[!UICONTROL 电子邮件]**&#x200B;命名空间。 单击&#x200B;**[!UICONTROL 应用]**。
   ![](assets/test-profiles-4bis.png)
1. 选择架构并在&#x200B;**[!UICONTROL 架构属性]**&#x200B;窗格中启用&#x200B;**[!UICONTROL 配置文件]**&#x200B;选项。
   ![](assets/test-profiles-5.png)
1. 单击&#x200B;**保存**。

>[!NOTE]
>
>有关创建架构的更多信息，请参阅[XDM文档](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=zh-Hans#prerequisites){target="_blank"}。

### 创建数据集

然后，您需要&#x200B;**创建要在其中导入用户档案的数据集**。 执行以下步骤：

1. 浏览到&#x200B;**[!UICONTROL 数据集]**，然后单击&#x200B;**[!UICONTROL 创建数据集]**。
   ![](assets/test-profiles-6.png)
1. 选择&#x200B;**[!UICONTROL 从架构]**&#x200B;创建数据集。
   ![](assets/test-profiles-7.png)
1. 选择之前创建的架构，然后单击&#x200B;**[!UICONTROL 下一步]**。
   ![](assets/test-profiles-8.png)
1. 选择一个名称，然后单击&#x200B;**[!UICONTROL 完成]**。
   ![](assets/test-profiles-9.png)
1. 启用&#x200B;**[!UICONTROL 配置文件]**&#x200B;选项。
   ![](assets/test-profiles-10.png)

>[!NOTE]
>
> 有关创建数据集的详细信息，请参阅[目录服务文档](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=zh-Hans#getting-started){target="_blank"}。

## 产品内用例{#use-case-1}

从Adobe Journey Optimizer主页中，您可以利用产品用例中的测试配置文件。 此用例有助于创建测试用户档案，用于在发布之前测试历程。

![](assets/use-cases-home.png)

单击&#x200B;**[!UICONTROL 开始]**&#x200B;按钮开始实施用例。

需要以下信息：

1. **身份命名空间**： [身份命名空间](../audience/get-started-identity.md)用于唯一标识测试配置文件。 例如，如果电子邮件用于识别测试用户档案，则应选择身份命名空间&#x200B;**Email**。 如果唯一标识符是电话号码，则应选择身份命名空间&#x200B;**电话**。

2. **CSV文件**：包含要创建的测试配置文件列表的逗号分隔文件。 用例需要CSV文件的预定义格式，该文件包含要创建的测试用户档案列表。 文件中的每一行应按正确的顺序包含以下字段，如下所示：

   1. **人员ID**：测试配置文件的唯一标识符。 此字段的值应当反映所选的身份命名空间。 (例如，如果为身份命名空间选择了&#x200B;**电话**，则此字段的值应为电话号码。 同样，如果选择&#x200B;**电子邮件**，则此字段的值应为电子邮件)
   1. **电子邮件地址**：测试配置文件电子邮件地址。 （如果选择&#x200B;**电子邮件**&#x200B;作为身份命名空间，**人员ID**&#x200B;字段和&#x200B;**电子邮件地址**&#x200B;字段可能包含相同的值）
   1. **名字**：测试配置文件名字。
   1. **姓氏**：测试配置文件的姓氏。
   1. **城市**：测试配置文件居住城市
   1. **国家/地区**：测试用户档案居住国家/地区
   1. **性别**：测试个人资料性别。 可用值为&#x200B;**男**、**女**&#x200B;和&#x200B;**非指定**

选择身份命名空间并根据上述格式提供CSV文件后，选择右上角的&#x200B;**[!UICONTROL 运行]**&#x200B;按钮。 用例可能需要几分钟才能完成。 一旦用例完成处理和创建测试用户档案，将发送通知以通知用户。

>[!NOTE]
>
>测试配置文件可能会覆盖现有配置文件。 在执行用例之前，请确保CSV仅包含测试用户档案，并且它针对正确的沙盒执行。

## 将配置文件转换为测试配置文件{#turning-profile-into-test}

您可以将现有配置文件转换为测试配置文件：您可以使用与创建配置文件相同的方式更新配置文件属性。

一个简单的方法是在历程中使用&#x200B;**[!UICONTROL 更新配置文件]**&#x200B;操作活动，并将&#x200B;**testProfile**&#x200B;布尔字段从false更改为true。

您的历程将由&#x200B;**[!UICONTROL 读取受众]**&#x200B;和&#x200B;**[!UICONTROL 更新配置文件]**&#x200B;活动组成。 您首先需要创建一个受众，以定向要转换为测试用户档案的用户档案。

>[!NOTE]
>
> 由于您将更新&#x200B;**testProfile**&#x200B;字段，因此所选配置文件必须包含此字段。 相关架构必须具有&#x200B;**配置文件测试详细信息**&#x200B;字段组。 请参阅[此小节](../audience/creating-test-profiles.md#test-profiles-prerequisites)。

1. 浏览至&#x200B;**受众**，然后在右上角&#x200B;**创建受众**。
   ![](assets/test-profiles-22.png)
1. 定义受众的名称并构建受众：选择字段和值以定向您需要的用户档案。
   ![](assets/test-profiles-23.png)
1. 单击&#x200B;**保存**&#x200B;并检查受众是否正确定向了用户档案。
   ![](assets/test-profiles-24.png)

   >[!NOTE]
   >
   > 受众计算可能需要一些时间。 在[此章节](../audience/about-audiences.md)中详细了解受众。

1. 现在，创建一个新历程并开始一个&#x200B;**[!UICONTROL 读取受众]**&#x200B;编排活动。
1. 选择之前创建的受众以及您的配置文件使用的命名空间。
   ![](assets/test-profiles-25.png)
1. 添加&#x200B;**[!UICONTROL 更新配置文件]**&#x200B;操作活动。
1. 选择架构、**testProfiles**&#x200B;字段和数据集，并将值设置为&#x200B;**True**。 若要执行此操作，请在&#x200B;**[!UICONTROL VALUE]**&#x200B;字段中，单击右侧的&#x200B;**笔**&#x200B;图标，选择&#x200B;**[!UICONTROL 高级模式]**&#x200B;并输入&#x200B;**true**。
   ![](assets/test-profiles-26.png)
1. 单击&#x200B;**[!UICONTROL 发布]**。
1. 在&#x200B;**[!UICONTROL 受众]**&#x200B;部分中，检查配置文件是否已正确更新。
   ![](assets/test-profiles-28.png)

   >[!NOTE]
   >
   > 有关&#x200B;**[!UICONTROL 更新配置文件]**&#x200B;活动的详细信息，请参阅[此部分](../building-journeys/update-profiles.md)。

## 使用csv文件创建测试配置文件{#create-test-profiles-csv}

在Adobe Experience Platform中，您可以通过将包含其他配置文件字段的csv文件上传到数据集来创建配置文件。 这是最简单的方法。

1. 使用电子表格软件创建一个简单的csv文件。
1. 为每个所需的字段添加一列。 确保添加主标识字段（上面示例中为“personID”），并将“testProfile”字段设置为“true”。
   ![](assets/test-profiles-11.png)
1. 为每个用户档案添加一行并填写每个字段的值。
   ![](assets/test-profiles-12.png)
1. 将电子表格另存为csv文件。 确保使用逗号作为分隔符。
1. 浏览到Adobe Experience Platform **工作流**。
   ![](assets/test-profiles-14.png)
1. 选择&#x200B;**将CSV映射到XDM架构**，然后单击&#x200B;**启动**。
   ![](assets/test-profiles-16.png)
1. 选择要将用户档案导入到的数据集。 单击&#x200B;**下一步**。
   ![](assets/test-profiles-17.png)
1. 单击&#x200B;**选择文件**&#x200B;并选择您的csv文件。 上传文件后，单击&#x200B;**下一步**。
   ![](assets/test-profiles-18.png)
1. 将源csv字段映射到架构字段，然后单击&#x200B;**完成**。
   ![](assets/test-profiles-19.png)
1. 数据导入开始。 状态将从&#x200B;**正在处理**&#x200B;移至&#x200B;**成功**。 单击右上方的&#x200B;**预览数据集**。
   ![](assets/test-profiles-20.png)
1. 检查测试配置文件是否已正确添加。
   ![](assets/test-profiles-21.png)

您的测试用户档案已添加，现在可以在测试历程时使用。 请参阅[此小节](../building-journeys/testing-the-journey.md)。


>[!NOTE]
>
>有关csv导入的详细信息，请参阅[数据摄取文档](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=zh-Hans#tutorials){target="_blank"}。
>


## 使用API调用创建测试用户档案{#create-test-profiles-api}

您还可以通过API调用创建测试用户档案。 在 [Adobe Experience Platform 文档](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=zh-Hans){target="_blank"}中了解详情。

您必须使用包含“配置文件测试详细信息”字段组的配置文件架构。 testProfile标志是此字段组的一部分。
创建配置文件时，请确保传递值： testProfile = true。

请注意，您还可以更新现有配置文件，将其testProfile标志更改为“true”。

以下是创建测试用户档案的API调用示例：

```
curl -X POST \
'https://dcs.adobedc.net/collection/xxxxxxxxxxxxxx' \
-H 'Cache-Control: no-cache' \
-H 'Content-Type: application/json' \
-H 'Postman-Token: xxxxx' \
-H 'cache-control: no-cache' \
-H 'x-api-key: xxxxx' \
-H 'x-gw-ims-org-id: xxxxx' \
-d '{
"header": {
"msgType": "xdmEntityCreate",
"msgId": "xxxxx",
"msgVersion": "xxxxx",
"xactionid":"xxxxx",
"datasetId": "xxxxx",
"imsOrgId": "xxxxx",
"source": {
"name": "Postman"
},
"schemaRef": {
"id": "https://example.adobe.com/mobile/schemas/xxxxx",
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"contentType": "application/vnd.adobe.xed-full+json;version=1"
}
},
"xdmEntity": {
"_id": "xxxxx",
"_mobile":{
"ECID": "xxxxx"
},
"testProfile":true
}
}
}'
```

## 操作说明视频 {#video}

了解如何创建测试用户档案。

>[!VIDEO](https://video.tv.adobe.com/v/3416329?quality=12&captions=chi_hans)
