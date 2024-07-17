---
title: 使用电子邮件垃圾邮件报告
description: 了解如何使用电子邮件垃圾邮件报告。
feature: Preview
role: User
level: Beginner
badge: label="Beta 版"
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 5f69b252f5812f43b3d0a6fed0aac074ece0d10f
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 24%

---

# 垃圾邮件报告 {#spam-report}

>[!CONTEXTUALHELP]
>id="ajo_simulate_spam_report"
>title="垃圾邮件报告"
>abstract="垃圾邮件报告可让您检查电子邮件内容垃圾邮件评分。此分数表明 ISP 或邮箱提供商是否会将您的邮件视为垃圾邮件。分数越低越好。如果您的电子邮件内容分数高于 2，您应该考虑修复导致测试失败的问题。"

您可以在专用的垃圾邮件报告中检查您的电子邮件内容垃圾邮件评分。 使用[SpamAssassin](https://spamassassin.apache.org/){target="_blank"}，Adobe Journey Optimizer可以测试您的电子邮件内容并为其打分，以指示ISP或邮箱提供商是否将其视为垃圾邮件。

>[!AVAILABILITY]
>
>此功能目前为 Beta 版，仅供 Beta 版客户使用。要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

在编辑或预览电子邮件内容时，**[!UICONTROL 垃圾邮件报告]**&#x200B;按钮会提供评分和建议以提高列出的每个项目的分数。

此功能允许您确定邮件在接收时是否会被反垃圾邮件工具视为垃圾邮件，并在出现这种情况时执行操作。 许多电子邮件收件箱提供商使用工具作为其垃圾邮件过滤流程的一部分。 发送得分不佳的电子邮件可能会严重影响您的可投放性。

要访问&#x200B;**[!UICONTROL 垃圾邮件报告]**，请执行以下步骤。

1. 在&#x200B;**[!UICONTROL 模拟]**&#x200B;屏幕中，单击&#x200B;**[!UICONTROL 垃圾邮件报告]**&#x200B;按钮。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 自动执行反垃圾邮件检查，**[!UICONTROL 垃圾邮件报告]**&#x200B;窗口显示结果。 它可以在正文布局、结构、图像大小、垃圾邮件触发词（如果有）等方面显示您内容的运行情况。

   ![](assets/spam-report-high-score.png)

1. 检查每个项目的得分和描述。

   分数越低越好。如果得分高于5，则会显示警告：表示某些邮件在收到时可能被阻止或标记为垃圾邮件。 最佳实践为分数小于2。

1. 根据该得分，如果您认为某些元素可以改进，请在[电子邮件Designer](../email/content-from-scratch.md)中编辑您的内容并进行必要的更新。

1. 完成更改后，浏览回&#x200B;**[!UICONTROL 垃圾邮件报告]**&#x200B;屏幕以确保分数提高。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
