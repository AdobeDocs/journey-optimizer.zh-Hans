---
solution: Journey Optimizer
product: journey optimizer
title: 为自己的电子邮件内容编写代码
description: 了解如何为自己的电子邮件内容编写代码
feature: Email Design
topic: Content Management
role: User
level: Intermediate, Experienced
keywords: 代码，HTML，编辑器
exl-id: 5fb79300-08c6-4c06-a77c-d0420aafca31
source-git-commit: 48b3ef3d2e041ea49d1b0c91cc72ea04237a5e33
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 34%

---

# 对您自己的内容进行编码 {#code-content}

使用&#x200B;**[!UICONTROL 自己编写代码]**&#x200B;模式导入原始 HTML 和/或为电子邮件内容编写代码。此方法需要 HTML 技能。

➡️ [通过观看视频了解此功能](#video)

>[!CAUTION]
>
> 使用此方法时，无法引用[Adobe Experience Manager Assets](../integrations/assets.md)中的图像。 在HTML代码中引用的图像必须存储在公共位置。

1. 从电子邮件Designer主页中，选择&#x200B;**[!UICONTROL 自己编写代码]**。

   ![](assets/code-your-own.png)

1. 输入或粘贴您的原始 HTML 代码。

1. 使用左窗格利用[!DNL Journey Optimizer]个性化功能。 [了解详情](../personalization/personalize.md)

   ![](assets/code-editor.png)

   >[!NOTE]
   >
   >与旅程表达式相比，电子邮件Designer中的个性化编辑器存在一些功能限制。 [了解有关日期/时间函数限制的更多信息](#date-time-limitations)

1. 如果要清除电子邮件内容并从新的设计编写电子邮件内容，请从选项菜单中选择&#x200B;**[!UICONTROL 更改您的设计]**。

   ![](assets/code-editor-change-design.png)

   >[!NOTE]
   >
   >此操作将在电子邮件设计器中打开选定的模板。您可以在其中完成电子邮件的设计，或使用&#x200B;**[!UICONTROL 切换到代码编辑器]**&#x200B;选项来返回代码编辑器。

1. 单击&#x200B;**[!UICONTROL 预览]**&#x200B;按钮以使用测试用户档案检查邮件设计和个性化。 [了解详情](../content-management/preview-test.md)

   ![](assets/code-editor-preview.png)

1. 在代码就绪后，单击&#x200B;**[!UICONTROL 保存]**，然后返回消息创建屏幕以完成消息。

   ![](assets/code-editor-save.png)

## 日期和时间函数限制 {#date-time-limitations}

在Email Designer代码编辑器中使用个性化设置时，`now()`函数不可用于动态日期计算。

>[!IMPORTANT]
>
>在电子邮件生成器的表达式语言中，`now()`函数是&#x200B;**不支持**。 虽然`now()`在历程条件中可用，但它不能在电子邮件内容或代码编辑器中使用。

**可用替代项：**

使用以下功能处理电子邮件个性化中的当前日期和时间：

* **`getCurrentZonedDateTime()`** — 返回包含时区信息的当前日期和时间。 这是`now()`的推荐替代方案。

  示例： `{%= getCurrentZonedDateTime() %}`返回`2024-12-06T17:22:02.281067+05:30[Asia/Kolkata]`

* **`currentTimeInMillis()`** — 返回当前时间（以纪元毫秒为单位）。

  示例：`{%= currentTimeInMillis() %}`

**建议的解决方法：**

如果需要在电子邮件内容中执行日期计算：

* **预先计算日期字段** — 在发送电子邮件之前，计算数据管道或配置文件属性中所需的日期值，然后在个性化设置中引用这些预先计算的值。

  示例：`{%= profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate %}`

* **使用日期操作函数** — 使用配置文件属性中日期值的[日期/时间函数](../personalization/functions/dates.md)（如`dayOfYear()`或`diffInDays()`）。

  示例：`{%= formatDate(profile.timeSeriesEvents._mobile.hotelBookingDetails.bookingDate, "MM/dd/YY") %}`

* **使用计算属性** — 创建执行复杂日期计算的[计算属性](../audience/computed-attributes.md)，使结果可用作配置文件属性。

了解个性化设置[中](../personalization/functions/dates.md)日期时间函数的更多信息。
