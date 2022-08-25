---
title: '更改主电子邮件地址 '
description: 了解如何从用户档案服务确定要使用的电子邮件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 更改主地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定义要使用的地址"
>abstract="当数据库中有多个地址（个人地址、专业地址等）可用时，您可以选择要优先发送的地址。"

定位用户档案时，数据库中可能有多个电子邮件地址或电话号码（专业电子邮件地址、个人电话号码等）。

使用 [!DNL Journey Optimizer]，您可以确定从用户档案服务中使用的电子邮件地址或电话号码，并在多个地址可用时排定优先级。 为此，请执行以下步骤：

1. 访问 **[!UICONTROL Channels]** > **[!UICONTROL General]** > **[!UICONTROL Executions fields]** 菜单。

   ![](assets/primary-address-execution-fields.png)

1. 默认情况下，当前用于确定用户档案电子邮件地址和电话号码的字段会显示在此屏幕上。 单击 **[!UICONTROL Edit]** 来改变他们。

   ![](assets/primary-address.png)

1. 单击所选的当前字段或编辑图标以选择新字段。

   ![](assets/primary-address-edit.png)

1. 此时会显示可用电子邮件类型XDM字段的列表。 选择要使用的字段。

   ![](assets/primary-address-select-field.png)

1. 单击 **[!UICONTROL Save]** 以确认您的选择。

执行字段已更新，现在将用作主地址。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
