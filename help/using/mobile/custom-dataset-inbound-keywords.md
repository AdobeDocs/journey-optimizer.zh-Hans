---
solution: Journey Optimizer
product: journey optimizer
title: 入站关键字的自定义数据集
description: 了解如何使用Experience Platform架构、数据集和短信API凭据在Adobe Journey Optimizer中启用用户档案的自定义数据集中存储入站SMS关键字。
feature: SMS, Channel Configuration
role: Admin
level: Intermediate
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: d6e5c7fd-c1d6-4137-98cd-138ccde6752f
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 518
ht-degree: 8%

---

# 对入站关键词使用自定义数据集 {#custom-dataset-inbound-keywords}

入站SMS关键字可以存储在启用用户档案的自定义数据集中。 该配置包含Adobe Experience Platform架构、从该架构创建的数据集，以及引用入站消息数据集的Journey Optimizer SMS API凭据。

>[!NOTE]
>
>如果未配置自定义数据集，则默认情况下将入站关键字存储在系统&#x200B;_AJO入站活动事件数据集_&#x200B;中。 在此数据集中捕获传入消息之前，配置文件必须至少从[!DNL Journey Optimizer]发送一条消息。 [了解有关系统数据集的更多信息](../data/get-started-datasets.md#system-datasets)

有关架构、字段组和数据集的背景，请参阅以下Adobe Experience Platform文档：

* [XDM系统概述](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=zh-Hans){target="_blank"}
* [架构构成基础](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=zh-Hans){target="_blank"}
* [数据集概述](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=zh_Hans){target="_blank"}

要将自定义数据集用于入站关键词，您需要：

1. [创建架构](#create-schema)
1. [创建数据集](#create-dataset)
1. [配置API凭据](#configure-api-credentials)

## 创建架构 {#create-schema}

架构定义适用于所摄取数据的结构和验证规则。 通过添加下面列出的现有字段组，为入站关键词集合构建体验事件架构。

➡️ [在Adobe Experience Platform文档中了解有关架构创建的更多信息](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/schema/composition)

1. 在Adobe Experience Platform中，从&#x200B;**[!UICONTROL 数据管理]**&#x200B;访问&#x200B;**[!UICONTROL 架构]**&#x200B;并选择&#x200B;**[!UICONTROL 创建架构]**。

   ![](assets/schema-sms-1.png)

1. 选择&#x200B;**[!UICONTROL 标准架构]**。

1. 选择&#x200B;**[!UICONTROL 体验事件]**。

   ![](assets/schema-sms-2.png)

1. 输入架构的&#x200B;**[!UICONTROL 显示名称]**，然后单击&#x200B;**[!UICONTROL 完成]**。

   这将保存架构并打开架构编辑器。

1. 打开&#x200B;**[!UICONTROL 架构属性]**&#x200B;并启用&#x200B;**[!UICONTROL 配置文件]**&#x200B;的架构。

   ![](assets/schema-sms-3.png)

1. 在&#x200B;**[!UICONTROL 字段组]**&#x200B;中，添加这些现有的字段组：

   * [!DNL Adobe CJM ExperienceEvent - Message interaction details]
   * [!DNL Adobe CJM ExperienceEvent - Message Execution Details]
   * [!DNL Adobe CJM ExperienceEvent - Message Profile Details]

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 创建数据集 {#create-dataset}

数据集是所摄取数据的存储容器。 每个数据集只与一种架构关联，写入数据集的记录必须符合该架构。

1. 在Adobe Experience Platform中，从&#x200B;**[!UICONTROL 数据管理]**&#x200B;访问&#x200B;**[!UICONTROL 数据集]**&#x200B;并选择&#x200B;**[!UICONTROL 创建数据集]**。

   ![](assets/schema-sms-4.png)

1. 选择&#x200B;**[!UICONTROL 从架构]**&#x200B;创建数据集。

1. 选择在上一部分中创建的架构，然后单击&#x200B;**[!UICONTROL 下一步]**。

   ![](assets/schema-sms-5.png)

1. 输入&#x200B;**[!UICONTROL 名称]**&#x200B;并单击&#x200B;**[!UICONTROL 完成]**。

1. 从&#x200B;**[!UICONTROL 数据活动]**&#x200B;选项卡，启用&#x200B;**[!UICONTROL 配置文件]**&#x200B;的数据。

   选择适合组织治理要求的&#x200B;**[!UICONTROL 数据保留]**&#x200B;策略。

   ![](assets/schema-sms-6.png)

1. 单击&#x200B;**[!UICONTROL 保存]**。

## 配置API凭据 {#configure-api-credentials}

使用[开始使用短信/彩信/RCS配置](mobile-configuration.md)，根据短信提供商配置凭据。 然后，完成以下步骤以选择自定义集客数据集。

1. 在左边栏中，浏览到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** `>` **[!UICONTROL SMS设置]**&#x200B;并选择&#x200B;**[!UICONTROL API凭据]**&#x200B;菜单。 单击&#x200B;**[!UICONTROL 创建新API凭据]**&#x200B;按钮。

1. 创建或编辑凭据，具体取决于您的提供商。

1. 启用&#x200B;**[!UICONTROL 为入站]**&#x200B;使用自定义数据集选项。

1. 选择在上一部分中创建的&#x200B;**[!UICONTROL 数据集]**。

   ![](assets/schema-sms-7.png)

1. 填写所有其余必填字段，然后单击&#x200B;**[!UICONTROL 保存]**。

   >[!NOTE]
   >
   >保存API凭据后，Journey Optimizer会验证入站关键词数据集是否已正确配置。 如果验证失败，则会显示一条错误消息，指示所需的更正。

保存凭据后，出站和入站消息传递行为保持不变；该凭据的入站关键字会记录在选定的自定义数据集中。
