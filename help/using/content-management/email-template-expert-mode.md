---
solution: Journey Optimizer
product: journey optimizer
title: 使用高级HTML编辑器编辑电子邮件模板
description: 使用专家模式在WYSIWYG编辑器中查看和编辑电子邮件内容的HTML源，具有功能标志控制、护栏和保存验证。
feature: Templates
topic: Content Management
role: User
hidefromtoc: true
hide: true
level: Experienced
source-git-commit: 74102069afa519898149de33f890568950571f26
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 5%

---

# 使用高级HTML编辑器编辑电子邮件模板 {#email-template-expert-mode}

>[!AVAILABILITY]
>
>此功能为限量发布版。请联系 Adobe 代表获取访问权限。

**高级HTML编辑器**&#x200B;是一种专家模式，允许您直接从[!DNL Journey Optimizer]电子邮件Designer界面查看和编辑电子邮件内容模板的原始源代码。

此功能允许您直接在源中插入高级表达式（如条件）。 切换回可视化（桌面）视图后，内容将重新呈现，这样您就可以检查内容的外观，并在任一视图中继续编辑。

>[!NOTE]
>
>此功能仅在内容模板和电子邮件渠道中可用。

## 护栏 {#guardrails}

使用高级HTML编辑器时，请遵循以下护栏来保护内容兼容性并设置期望值。

* 当前，高级HTML编辑器中&#x200B;**没有验证进程**。 不检查语法错误和中断的布局。 在保存之前，请确保仔细查看您的内容。

* 将来的系统更新可能会恢复对默认标记所做的更改。 请注意，**您的更改可能被覆盖**。

* 自定义代码和手动更改导致的问题&#x200B;**无法由**&#x200B;支持团队排除或解决[!DNL Adobe]。 如果需要还原到以前的版本，请确保您拥有内容的备份。

* 为确保内容兼容性，在高级HTML视图中&#x200B;**保存不可用**。 准备好保存更改后，必须切换回“桌面”视图。

>[!WARNING]
>
>内容模板中的高级HTML编辑器与电子邮件Designer中的&#x200B;**[!UICONTROL 为自己编码]**&#x200B;模式不同。 在[!UICONTROL 对您自己的]模式进行编码，您无法切换回可视编辑器 — 一旦选择该路径，您将处于仅进行代码编辑的状态。 相比之下，高级HTML编辑器允许您随时在HTML视图和桌面（可视化）视图之间切换。 [详细了解代码编辑器](../email/code-content.md)

## 切换到高级HTML视图 {#switch-to-desktop-view}

1. 打开或创建[电子邮件模板](../content-management/create-content-templates.md)并打开[电子邮件Designer](../email/get-started-email-design.md)以编辑内容。

1. 单击屏幕右上角的&#x200B;**[!UICONTROL HTML]**&#x200B;按钮。

   ![](assets/email-template-expert-mode-button.png)

1. 首次打开高级HTML编辑器时，会显示一条警告消息。 请仔细查看并单击&#x200B;**[!UICONTROL 确定]**&#x200B;以继续。 [了解详情](#guardrails)

   >[!NOTE]
   >
   >仅当您首次打开高级HTML编辑器并每月重置时，此警告才会显示。

   ![](assets/email-template-expert-mode-warning.png)

1. 此时将显示高级HTML编辑器。

   ![](assets/email-template-expert-mode.png)

1. 将所需的更改添加到您的电子邮件内容中。

   >[!WARNING]
   >
   >确保输入正确的HTML和CSS代码，因为没有语法验证过程，[!DNL Adobe]也不提供支持。 [了解详情](#guardrails)

1. 在高级HTML视图中无法保存。 切换回“桌面”视图以保存更改。

   &lt;![](assets/email-template-expert-mode-save.png)

   >[!NOTE]
   >
   >出于内容兼容性的原因，只能将内容保存在桌面视图中。 切换视图时，将保留所做的编辑。
