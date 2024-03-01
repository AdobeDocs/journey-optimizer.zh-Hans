---
solution: Journey Optimizer
product: journey optimizer
title: 更改执行地址
description: 了解如何从配置文件服务确定要使用的电子邮件地址。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 主要，执行，电子邮件，目标，用户档案，优化器
exl-id: fe2f6516-7790-4501-a3a1-3d7cb94d7874
source-git-commit: 9cc263d127fdc56f808770d908030b1d14b1f784
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 18%

---

# 更改执行地址 {#change-primary-email}

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address"
>title="定义要使用的地址"
>abstract="当数据库中有多个电子邮件地址或电话号码（个人、职业等）时，您可以选择优先向哪个电子邮件地址或电话号码发送。"

>[!CONTEXTUALHELP]
>id="ajo_admin_execution_address_header"
>title="定义要使用的地址"
>abstract="编辑字段，该字段用于确定优先向其发送的配置文件的电子邮件地址或电话号码。"

定向用户档案时，数据库中可能会提供多个电子邮件地址或电话号码（专业电子邮件地址、个人电话号码等）。

在这种情况下， [!DNL Journey Optimizer] 用途 **[!UICONTROL 执行字段]** 以确定从配置文件服务中优先使用的电子邮件地址或电话号码。

要检查当前默认使用的字段，请访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 常规]** > **[!UICONTROL 执行字段]** 菜单。

![](assets/primary-address-execution-fields.png)

当前值用于沙盒级别的所有投放。 您可以根据需要更新这些字段。

在大多数情况下，您将全局更改执行字段，并定义一个应用于所有电子邮件或短信消息的值。 <!--[Learn how](#admin-settings)-->

<!--In some specific use cases only, you can override the value set globally and define a different value at the journey level. [Learn more](#journey-parameters)-->

## 更新管理设置 {#admin-settings}

要在沙盒级别全局更改执行字段，请执行以下步骤。

1. 访问  **[!UICONTROL 渠道]** > **[!UICONTROL 常规]** > **[!UICONTROL 执行字段]** 菜单。

1. 单击 **[!UICONTROL 编辑]** 以更改默认值。

   ![](assets/primary-address.png)

1. 单击您选择的当前字段或编辑图标以选择新字段。

   ![](assets/primary-address-edit.png)

1. 此时将显示可用电子邮件类型XDM字段的列表。 选择要使用的字段。

   ![](assets/primary-address-select-field.png)

1. 单击 **[!UICONTROL 保存]** 确认您的选择。

执行字段已更新，现在将用作主地址。

<!--1. You can also select an additional field to use as secondary email address. This allows you to determine which field to use if the primary field is empty for a profile. -->

## 覆盖历程参数中的值 {#journey-parameters}

仅对于特定用例，您可以全局覆盖执行字段设置，并在历程级别定义不同的值，尤其是电子邮件渠道的值。

添加 **[!UICONTROL 电子邮件]** 操作更改为 [历程](../email/create-email.md#create-email-journey-campaign)，主电子邮件地址会显示在历程高级参数下。

在某些特定上下文中，您可以使用覆盖此值 **[!UICONTROL 启用参数覆盖]** 图标（位于页面右侧） **[!UICONTROL 地址]** 字段。

![](assets/journey-enable-parameter-override.png)

>[!CAUTION]
>
>仅应针对特定用例使用电子邮件地址覆盖。大多数情况下，您无需更改电子邮件地址，因为值在中被定义为主地址。 **[!UICONTROL 执行字段]** 是应该使用的变量。

覆盖此值可能很有用，例如：

* 测试电子邮件。您可以添加自己的电子邮件地址：发布历程后，会向您发送电子邮件。
* 向列表的订阅者发送电子邮件。 在[此用例](../building-journeys/message-to-subscribers-uc.md)中了解更多。
