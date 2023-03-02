---
solution: Journey Optimizer
product: journey optimizer
title: 更改主要电子邮件地址
description: 了解如何从用户档案服务中确定要使用的电子邮件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，执行，电子邮件，目标，用户档案，优化器
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: b8065a68ed73102cb2c9da2c2d2675ce8e5fbaad
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 3%

---

# 更改主要地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定义要使用的地址"
>abstract="当有多个电子邮件地址或电话号码（个人、专业人员等）在数据库中可用时，您可以选择发送哪个电子邮件地址或电话号码的优先级。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定义要使用的地址"
>abstract="编辑用于确定用户档案电子邮件地址或电话号码的字段以优先发送。"

当您定位用户档案时，数据库中可能会提供多个电子邮件地址或电话号码（专业电子邮件地址、个人电话号码等）。

替换为 [!DNL Journey Optimizer]，您可以从配置文件服务中确定要使用的电子邮件地址或电话号码，并在有多个地址可用时进行优先排序。 为此，请执行以下步骤。

1. 访问  **[!UICONTROL 渠道]** > **[!UICONTROL 常规]** > **[!UICONTROL 执行字段]** 菜单。

   ![](assets/primary-address-execution-fields.png)

1. 当前默认用于确定用户档案的电子邮件地址和电话号码的字段将显示在此屏幕上。 单击 **[!UICONTROL 编辑]** 来改变它们。

   ![](assets/primary-address.png)

1. 单击您选择的当前字段或编辑图标以选择新字段。

   ![](assets/primary-address-edit.png)

1. 此时将显示可用电子邮件类型XDM字段的列表。 选择要使用的字段。

   ![](assets/primary-address-select-field.png)

1. 单击 **[!UICONTROL 保存]** 以确认您的选择。

执行字段已更新，现在将用作主地址。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->
