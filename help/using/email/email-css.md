---
solution: Journey Optimizer
product: journey optimizer
title: 向电子邮件内容添加自定义CSS
description: 了解如何直接在Journey Optimizer的Email Designer中将自定义CSS添加到您的电子邮件内容中
feature: Email Design
topic: Content Management
role: User
level: Intermediate
keywords: css，编辑器，摘要，电子邮件
source-git-commit: feb3576c230f2fb28ab031f87cc5f99263329b57
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 3%

---

# 将元数据添加到您的电子邮件内容 {#email-metadata}

>[!CONTEXTUALHELP]
>id="ac_edition_css"
>title="添加自定义CSS"
>abstract="xxx."

在设计电子邮件时，您可以直接在[!DNL Journey Optimizer] [电子邮件Designer](get-started-email-design.md)中添加自己的自定义CSS。

添加自定义CSS文本区域中应包含有效的CSS字符串。

![](assets/email-body-css.png)

可用性条件

添加自定义CSS功能仅在编辑器中定义内容时可用。 要查看添加自定义CSS部分，用户需要在编辑器中添加内容。 如果用户删除其所有内容，则该部分将消失，并且不会应用自定义css。 如果用户将内容添加回，则部分将可用并且应用自定义css。

**无效CSS输入的示例**

无法保存无效的CSS，如果CSS无效，将显示一个红色的toast以指示无法保存CSS。

`<style>`未被接受


```
<style type="text/css">
  .acr-Form {
    width: 100%;
    padding: 20px 100px;
    border-spacing: 0px 8px;
    box-sizing: border-box;
    margin: 0;
  }
</style>
```


缺少大括号无效

```
body {
 background: red; 
```
