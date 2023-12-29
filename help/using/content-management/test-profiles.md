---
title: 选择测试用户档案
description: 了解如何选择测试用户档案以预览和测试内容。
feature: Preview, Proofs
role: User
level: Beginner
exl-id: c51e4089-7f51-437d-a5ed-de10bab46cf8
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 16%

---

# 选择测试用户档案 {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_preview_test_profiles"
>title="使用测试配置文件检查您的内容"
>abstract="使用测试配置文件预览和测试您的内容。如果您添加了个性化字段，则可以使用测试配置文件数据检查它们的显示方式。"

在预览或测试内容之前，您首先需要选择测试用户档案，这些是与定义的定位标准不匹配的附加收件人。 [了解如何创建测试用户档案](../audience/creating-test-profiles.md)

要选择测试用户档案，请执行以下步骤：

1. 从消息的编辑内容屏幕或Email Designer中，单击 **[!UICONTROL 模拟内容]** 按钮。

1. 单击 **[!UICONTROL 管理测试用户档案]** 按钮，然后单击 **[!UICONTROL 身份命名空间]** 选择图标。 [了解有关Adobe Experience Platform身份命名空间的更多信息](../audience/get-started-identity.md).

   在以下示例中，我们使用 **电子邮件** 命名空间。

   ![](../email/assets/previewselect-namespace.png)

1. 使用搜索字段查找命名空间，将其选中并单击 **[!UICONTROL 选择]**

   ![](../email/assets/preview-email-namespace.png)

1. 在 **[!UICONTROL 标识值]** 字段中，输入用于标识测试用户档案的值（此处为电子邮件地址），然后单击 **[!UICONTROL 添加配置文件]**.

   <!--![](assets/preview-identity-value.png)-->

1. 如果您为消息添加了个性化设置，请添加其他用户档案，以便根据用户档案数据测试消息的不同变体。 添加后，用户档案会列在选定字段下。

   ![](../email/assets/preview-profile-list.png)

   此列表根据消息个性化元素，在相关列中显示每个测试用户档案的数据。
