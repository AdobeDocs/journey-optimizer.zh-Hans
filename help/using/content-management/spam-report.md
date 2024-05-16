---
title: 使用垃圾邮件报告
description: 了解如何使用垃圾邮件报告。
feature: Preview
role: User
level: Beginner
badge: label="Beta 版"
hide: true
hidefromtoc: true
exl-id: 9ab43b14-41cf-49f1-bdcf-6fee58db5000
source-git-commit: 4c1dca7815594bbbf5a2d84682338e8b2d743965
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 0%

---

# 电子邮件垃圾邮件报告 {#spam-report}

[!DNL Journey Optimizer] 使您能够检查内容对垃圾邮件过滤的表现如何，并确保您的邮件进入客户的收件箱 — 而不是垃圾邮件。

编辑或预览电子邮件内容时， **[!UICONTROL 垃圾邮件报告]** 选项提供评分和建议，以提高所列每个项目的得分。

这样，您就可以确定邮件在接收时是否会被反垃圾邮件工具视为垃圾邮件，如果不是这样，您可以采取相应的措施。 许多电子邮件收件箱提供商使用工具作为其垃圾邮件过滤流程的一部分。 发送得分不佳的电子邮件可能会严重影响您的可投放性。


>[!CAUTION]
>
>* 此功能目前仅作为专用测试版提供。
>
>* 目前，只能对英文内容执行垃圾邮件报告分析。
>
>* 垃圾邮件报告提供了有用信息，不会阻止发送得分不好的消息。

要访问 **[!UICONTROL 垃圾邮件报告]**，请按照以下步骤操作。

1. 从 **[!UICONTROL 模拟]** 屏幕上，单击 **[!UICONTROL 垃圾邮件报告]** 按钮。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 自动执行反垃圾邮件检查，并且 **[!UICONTROL 垃圾邮件报告]** 窗口显示结果。 它可以在正文布局、结构、图像大小、垃圾邮件触发词（如果有）等方面显示您内容的运行情况。

   ![](assets/spam-report-high-score.png)

1. 检查每个项目的得分和描述。

   分数越低越好。 如果得分高于5，则会显示警告：表示某些邮件在收到时可能被阻止或标记为垃圾邮件。

1. 根据该得分，如果您认为某些元素可以改进，请在以下位置编辑您的内容： [电子邮件设计工具](../email/content-from-scratch.md) 并进行必要的更新。

1. 完成更改后，浏览回 **[!UICONTROL 垃圾邮件报告]** 屏幕以确保您的分数得到改善。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->
