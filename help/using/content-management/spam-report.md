---
title: 使用垃圾邮件报告
description: 了解如何使用垃圾邮件报告。
feature: Preview
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: b6872806b3961bb2afbfc03999d984384492cc6d
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 2%

---

# 使用垃圾邮件报告 {#spam-report}

>[!AVAILABILITY]
>
>目前，垃圾邮件报告功能仅作为测试版提供给部分用户使用。 要加入 Beta 版计划，请联系 Adobe 客户关怀团队。

[!DNL Journey Optimizer] 使您能够检查内容对垃圾邮件过滤的表现如何，并确保您的邮件进入客户的收件箱 — 而不是垃圾邮件。

>[!CAUTION]
>
>* 此功能当前仅适用于电子邮件渠道。
>
>* 目前，只能对英文内容执行垃圾邮件报告分析。

编辑或预览内容时， **[!UICONTROL 垃圾邮件报告]** 选项提供评分和建议，以提高所列每个项目的得分。

这样，您就可以确定邮件在接收时是否会被反垃圾邮件工具视为垃圾邮件，如果不是这样，您可以采取相应的措施。

>[!CAUTION]
>
>“Spam（垃圾邮件）”报告仅提供指示和警告。 请注意，如果垃圾邮件报告指示您的内容被视为垃圾邮件，则不会阻止您发送邮件。 根据得分和改进建议采取相应措施是您的选择。

要使用 **[!UICONTROL 垃圾邮件报告]** 功能，请按照以下步骤操作。

<!--For example spam scoring tool can tell that there are too many Images compared to the text. Retailers tend to do this even though the spam score gets worse because the content is more engaging.-->

<!--Michael, who is a marketer with NIKE works along with Tara from testing team to ensure that the emails being sent as part of the campaign/journey don't get categorised as SPAM.

They need an integration within AJO's marketing system to show how the curated content is doing against different SPAM compliance pillars like for SPAM trigger words, HTML Body content and layout, subject line etc.

They should be able to get scores for each individual items as shown by market standard SPAM filtering tools like Spam Assassin, Symantec etc.

They should also get suggestions on how to improve the score better to be confident that the messages don't get categorised as spam.-->

1. 从 **[!UICONTROL 模拟]** 屏幕上，单击 **[!UICONTROL 垃圾邮件报告]** 按钮。

   ![](assets/spam-report-button.png)

<!--
    You can also open the [Email Designer](../email/content-from-scratch.md), click the **[!UICONTROL More]** button and select **[!UICONTROL Check spam score]** from the menu.

    ![](assets/spam-report-check-score.png)
-->

1. 自动执行反垃圾邮件检查，并且 **[!UICONTROL 垃圾邮件报告]** 窗口显示结果。 它可以在正文布局、结构、图像大小、垃圾邮件触发词（如果有）等方面显示您内容的运行情况。

   ![](assets/spam-report-high-score.png)

1. 检查每个项目的得分和描述。

   如果得分高于5，则会显示警告。 它表示当收到某些邮件时，反垃圾邮件工具可能会阻止这些邮件或将其标记为垃圾邮件。

1. 根据该得分，如果您认为某些元素可以改进，请使用转到您的内容 [电子邮件设计工具](../email/content-from-scratch.md) 并进行所需的更新。

1. 完成更改后，返回至 **[!UICONTROL 垃圾邮件报告]** 屏幕以确保您的分数得到改善。

   ![](assets/spam-report-low-score.png)

<!--You can also check the message's alerts for warnings on potential risk of spam detection. Follow the steps below.

1. Click the **[!UICONTROL Alerts]** button on top right of the screen. [Learn more on email alerts](../email/create-email.md#check-email-alerts)

1. If **[!UICONTROL Spam checker alert]** is displayed, you should check your content for a potential risk of spam using the **[!UICONTROL Spam report]** feature as detailed above.

    ![](assets/spam-report-alert.png)
-->



