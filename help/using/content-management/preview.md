---
title: 预览您的内容
description: 了解如何预览内容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: 6477270c-0309-411a-8254-c7ffc4419492
source-git-commit: 03cb3298c905766bc059e82c58969a2111379345
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 3%

---

# 使用测试配置文件预览内容 {#preview}

<!--## Preview your content {#preview-content}-->

定义[测试用户档案](test-profiles.md)后，您可以预览内容。

>[!NOTE]
>
>[!DNL Journey optimizer]还允许您测试内容的不同变体，方法是预览内容并使用从CSV/JSON文件上传或手动添加的示例输入数据发送校样。 [了解如何使用示例输入数据测试内容](../test-approve/simulate-sample-input.md)

要使用测试用户档案预览内容，请执行以下步骤：

1. 从消息的编辑内容屏幕或电子邮件Designer中，单击&#x200B;**[!UICONTROL 模拟内容]**&#x200B;按钮。

1. 选择测试用户档案。 您可以检查列中的可用值。 使用右/左箭头浏览数据。

   ![](../email/assets/preview-select-profile.png)

   >[!NOTE]
   >
   >要添加更多测试配置文件，请选择&#x200B;**[!UICONTROL 管理测试配置文件]**。 [了解详情](test-profiles.md)

1. 单击列表上方的&#x200B;**[!UICONTROL 选择数据]**&#x200B;图标以添加或删除列。

   您可以在列表末尾看到特定于当前消息的个性化字段。 在本例中，就是用户档案的城市、名字和姓氏。 选择这些字段并确保在测试用户档案中填充这些值。

   ![](../email/assets/preview-select-data.png)

1. 在消息预览中，个性化的元素被替换为选定的测试用户档案数据。 例如，对于此消息，电子邮件内容和电子邮件主题都是个性化的：

   ![](../email/assets/preview-test-profile.png)

1. 选择其他测试用户档案以预览您电子邮件中每种消息变体的情况。

>[!NOTE]
>
>如果在配置详细信息中发现错误，请单击&#x200B;**[!UICONTROL 查看配置详细信息]**&#x200B;按钮。 [了解详情](../email/surface-personalization.md#check-configuration)

创建基于代码的体验时，您可以直接在浏览器或移动设备上预览个性化内容，以便进行实际模拟。 [了解详情](../code-based/create-code-based.md#preview-on-device)

