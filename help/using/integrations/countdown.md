---
solution: Journey Optimizer
product: journey optimizer
title: Dynamic media
description: 将Dynamic Media与Journey Optimizer结合使用
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: 707bc4053ee05c275b562e35227e54836e91fa27
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# 插入倒计时器 {#countdown}

使用Dynamic Media倒计时器创建紧迫感并最大限度地提高转化率，该计时器会在收件人打开您的电子邮件时实时更新。 此功能非常适用于闪电式销售、限时优惠和对时间敏感的促销活动。

例如，作为零售品牌的营销人员，您运行的是48小时闪购。 通过在促销电子邮件中使用倒计时器：

* 立即打开的收件人会看到“剩余47小时”
* 24小时后打开的收件人会看到“剩余23小时”
* 在销售结束后打开的收件人会看到“销售已结束”

有关如何在Adobe Experience Manager中创建Dynamic Media的详细信息，请参阅[本文档](assets/do-not-localize/countdown.pdf)。


1. 在&#x200B;**[!DNL Adobe Experience Manager]**&#x200B;中，创建一个Dynamic Media模板并为其添加一个倒计时器组件。

   ![](assets/timer-1.png)

1. 在&#x200B;**[!DNL Journey Optimizer]**&#x200B;中，创建新营销活动或打开现有营销活动，然后访问电子邮件Designer。

1. 将&#x200B;**[!UICONTROL HTML组件]**&#x200B;拖放到您的电子邮件内容中。

1. 选择&#x200B;**[!UICONTROL 显示源代码]**&#x200B;以直接编辑HTML。

   ![](assets/timer-2.png)

1. 从&#x200B;**[!UICONTROL 编辑HTML]**&#x200B;菜单中，导航到&#x200B;**[!UICONTROL Assets]**，然后单击&#x200B;**[!UICONTROL 打开资产选择器]**&#x200B;以浏览并选择您发布的Dynamic Media模板。

   ![](assets/timer-3.png)

1. 在&#x200B;**[!UICONTROL 自定义属性]**&#x200B;菜单中，根据需要为模板配置任何可自定义的URL参数。

   完成后单击&#x200B;**[!UICONTROL 保存]**。

   ![](assets/timer-4.png)

1. 在电子邮件Designer中选择资源，然后访问&#x200B;**[!UICONTROL 样式]**&#x200B;菜单。

   配置以下设置：
   * **横幅文本**：与计时器一起显示的文本
   * **结束时间**：倒计时过期的日期和时间。 仅以GMT（格林威治标准时间）输入时间。 系统不接受其他时区。
   * **回退文本**：计时器结束后显示的消息

   ![](assets/timer-5.png)

1. 单击&#x200B;**[!UICONTROL 预览]**&#x200B;查看包含实时倒计时更新的计时器并验证您的配置。

当收件人打开电子邮件时，他们会看到您的闪电促销的准确剩余时间。 如果他们稍后重新打开电子邮件，则倒计时会自动更新以反映当前剩余时间。 在结束日期之后，默认消息将自动显示。

