---
solution: Journey Optimizer
product: journey optimizer
title: 切换到深色模式
description: 了解如何在电子邮件Designer中使用深色模式
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 深色模式，电子邮件，颜色，编辑器
hide: true
hidefromtoc: true
exl-id: 27442cb0-5027-4d9c-9d3c-9ec33af7c9ff
source-git-commit: b5d9b9c26824517414982fa539e0b360500cafc6
workflow-type: tm+mt
source-wordcount: '1701'
ht-degree: 1%

---

# 管理深色模式内容 {#dark-mode}

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode"
>title="切换到深色模式"
>abstract="切换到深色模式，您可以在其中预览其呈现方式并定义特定的自定义设置。 <br>警告：最终渲染取决于收件人的电子邮件客户端。 并非所有电子邮件客户端都支持自定义深色模式。"

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_image"
>title="对深色模式使用特定图像"
>abstract="您可以选择在深色模式打开时显示的其他图像。 <br>注意：添加深色模式的特定图像无法保证它在所有电子邮件客户端中正确呈现。 并非所有电子邮件客户端都支持自定义深色模式。"

>[!CONTEXTUALHELP]
>id="ac_edition_darkmode_preview"
>title="切换到深色模式"
>abstract="切换到深色模式以预览它在支持的电子邮件客户端上可能呈现的方式。 <br>警告：最终渲染取决于收件人的电子邮件客户端。 并非所有电子邮件客户端都支持自定义深色模式。"

在设计电子邮件时，[!DNL Journey Optimizer] [电子邮件Designer](get-started-email-design.md)允许您切换到&#x200B;**[!UICONTROL 深色模式]**，您可以在其中定义特定的自定义设置。 当深色模式打开时，支持的电子邮件客户端将显示您为此模式定义的设置。

>[!WARNING]
>
>深色模式的最终呈现取决于收件人的电子邮件客户端。
>
>并非所有电子邮件客户端都支持自定义深色模式。 <!--[See the list](#non-supporting-email-clients)-->此外，某些电子邮件客户端只对收到的所有电子邮件应用其自己的默认深色模式。 在这种情况下，无法呈现您在Email Designer中定义的自定义设置。

[此部分](#supporting-email-clients)中显示了支持深色模式的电子邮件客户端列表。

## 什么是深色模式？ {#what-is-dark-mode}

深色模式允许受支持的电子邮件客户端和应用程序为文本、按钮和其他UI元素显示具有更暗背景和更浅颜色的电子邮件。 它可减少眼睛疲劳、节省电池续航时间，并改善在弱光环境中的可读性，以获得更舒适的观看体验。

<!--Dark Mode uses a dark color palette with light text and UI elements to reduce eye strain, save battery life, and improve readability in low-light environments.-->

随着主要操作系统和应用程序(Apple Mail、Gmail、Outlook、Twitter、Slack)的发展，电子邮件已成为现代电子邮件设计中的重要考虑因素，以确保内容清晰易读，并且所有用户都具有视觉吸引力。

但是，无法保证您的电子邮件在所有设备上在深色模式下看上去完全相同。 电子邮件应用程序或设备覆盖原始设计也可能会导致某些视觉更改。

事实上，电子邮件客户端应用深色模式的方式可能有所不同，如下所示<!--between different devices and apps-->：

* 并非所有电子邮件客户端都支持此功能。

  >[!NOTE]
  >
  >[此部分](#non-supporting-email-clients)中显示了不支持深色模式的电子邮件客户端列表。

* 某些电子邮件客户端会自动调整颜色、背景和图像。 在这种情况下，如果您在电子邮件Designer中定义自定义设置，则这些设置可能不会呈现。

* 其他电子邮件客户端提供了呈现自定义深色模式的选项（例如使用`@media (prefers-color-scheme: dark)`方法）。 在这种情况下，应显示您在电子邮件Designer中定义的特定设置。 在[本节](#define-custom-dark-mode)中了解如何在电子邮件Designer中定义自定义深色模式设置。

## 电子邮件Designer中的深色模式 {#dark-mode-email-designer}

在Email Designer中，当涉及到深色模式时，需要考虑两个方面：

* 您可以预览默认深色模式在大多数支持的电子邮件客户端中的呈现方式。 [了解详情](#preview-dark-mode)

<!--
    >[!CAUTION]
    >
    >The final rendering may vary according to the recipient's email client. To see the exact rendering for each email client, use the [Email rendering](../content-management/rendering.md) option.-->

* 如果要覆盖支持电子邮件客户端的默认设置，可以定义应用于正在编辑的电子邮件的自定义深色模式设置。 [了解详情](#define-custom-dark-mode)

<!--
    >[!WARNING]
    >
    >Not all email clients support custom dark mode. Some email clients only apply their own default dark mode for all emails that are received. In this case, the custom settings that you defined in the Email Designer cannot be rendered. [Learn more](#guardrails)-->

### 预览默认深色模式 {#preview-dark-mode}

要在Email Designer中访问深色模式并预览默认深色模式设置，请执行以下步骤。

1. 从电子邮件Designer主页中，选择&#x200B;**[!UICONTROL 从头开始设计]**&#x200B;选项。 [了解详情](content-from-scratch.md)

   >[!NOTE]
   >
   >当前，如果您选择[电子邮件模板](use-email-templates.md)或应用[主题](apply-email-themes.md)，则可能无法切换到深色模式。

1. 将[结构](content-from-scratch.md)和[内容组件](content-components.md)添加到您的内容中。

1. 在中心画布的右上角，将切换开关切换到&#x200B;**[!UICONTROL 深色模式]**。

   ![](assets/light-mode-toggle.png)

1. 默认深色模式预览显示。

   ![](assets/dark-mode-default.png)
<!--
    >[!NOTE]
    >
    >Dark mode applies to all elements, except images and icons.-->

默认情况下， Email Designer深色模式预览会将“全色反色”配色方案应用于除图像和图标之外的所有元素。<!--It fully inverts all colors for all the elements (texts, buttons, etc.)-->

这意味着它可以检测包含亮元素和暗元素的区域，并将它们反转，这样浅色背景变为深色，深色文本变为浅色，而深色背景变为浅色，浅色文本变为深色。

>[!CAUTION]
>
>最终渲染可能会因收件人的电子邮件客户端而异。 若要查看尽可能接近每个电子邮件客户端最终结果的模拟，请使用[电子邮件渲染](../content-management/rendering.md)选项。

<!--This is custom dark mode:

  ![](assets/dark-mode-custom.png)

Here you can see that we have applied a different background, defined another image and change the color of the text and button.-->

### 定义自定义深色模式 {#define-custom-dark-mode}

切换到&#x200B;**[!UICONTROL 深色模式]**&#x200B;后，您可以选择编辑内容的特定样式元素，这些样式元素仅在收件人的电子邮件客户端中启用深色模式时才会显示，前提是它支持该功能。

>[!WARNING]
>
>并非所有电子邮件客户端都支持深色模式。 此外，某些电子邮件客户端只对收到的所有电子邮件应用自己的默认深色模式。 在这两种情况下，无法呈现您在Email Designer中定义的自定义设置。

为了利用Email Designer自定义深色模式样式，Journey Optimizer使用<!-- `@media (prefers-color-scheme: dark)` method--> `@media (prefers-color-scheme: dark)` CSS查询，可检测用户的电子邮件客户端是否设置为深色模式，并应用电子邮件中定义的深色主题设计。

要定义自定义深色模式设置，请执行以下步骤。

1. 确保在电子邮件Designer中启用&#x200B;**[!UICONTROL 深色模式]**。 [了解如何操作](#preview-dark-mode)

1. 编辑任何样式颜色属性，如文本、背景、按钮等。

1. 您无法更改图像和图标的颜色，但只能为深色模式定义特定资产。 要执行此操作，请选择任意图像。 使用&#x200B;**[!UICONTROL 设置]**&#x200B;窗格中的专用切换开关切换到&#x200B;**[!UICONTROL 深色模式]**&#x200B;并选择其他资源。

   ![](assets/dark-mode-image.png)

   <!--![](assets/dark-mode-custom.png)-->

1. 您随时可以&#x200B;**[!UICONTROL 切换到实时视图]**，以便检查您的内容在各种设备大小上呈现的方式。 从该视图中，选择屏幕顶部的深色模式切换开关以预览不同设备上内容的深色模式版本。

   ![](assets/dark-mode-live-view.png){width="80%" align="center"}

   >[!CAUTION]
   >
   >实时视图是一个通用预览，用于比较呈现在各种设备大小中的外观。 最终渲染可能会因收件人的电子邮件客户端而异。

1. 对深色模式的更改感到满意后，单击&#x200B;**[!UICONTROL 模拟内容]**。

   ![](assets/dark-mode-simulate.png)

1. 选择&#x200B;**[!UICONTROL 渲染电子邮件]**&#x200B;并连接到您的Litmus帐户。 您可以看到各种电子邮件客户端的最终深色模式渲染。 了解有关[电子邮件渲染](../content-management/rendering.md)的更多信息。

   >[!WARNING]
   >
   >虽然模拟与电子邮件在深色模式中的显示方式非常接近，但实际呈现方式可能会因电子邮件服务提供商或设备级设置的不同而有所不同。

## 最佳实践 {#best-practices}

随着主要电子邮件客户端采用深色模式的次数增加，必须考虑您的电子邮件在浅色和深色环境中的呈现方式 — 无论您是否使用[自定义深色模式](#define-custom-dark-mode)。

深色模式可以改变颜色、背景和图像 — 有时会覆盖设计选择。 要确保可视一致性、可访问性和品牌完整性，请遵循下面列出的最佳实践。

**优化您的图像和徽标**

* 避免使用带有硬编码白色或浅色背景的图像。

* 将徽标和图标保存为具有透明背景的PNG，以避免在深色模式下显示白色框。

* 如果无法使用透明度，请将图像置于设计中的纯色背景上，以防止尴尬的颜色反转。

**观看您的背景**

* 确保文本颜色和背景颜色之间的对比度足以在浅色和深色模式下阅读。

* 避免仅依赖背景颜色处理关键内容。 某些客户端在深色模式下会覆盖背景颜色，因此请确保关键信息仍然可见。

**在深色模式下设计可访问的内容**

* 使用颜色组合，易于区分色盲人士。

* 使用中间调调色板确保与明暗背景的对比度。

* 使用具有高对比度的无障碍颜色组合以提高可读性并符合Web内容无障碍准则(WCAG)标准。 使用WebAIM的对比度检查器等工具验证颜色对比度。

* 避免使用细字体，因为它可能会影响可读性。 如果您的品牌需要细字体，请在深色模式下将其粗体。

* 跳过纯黑色的纯白色，因为它可能会导致眼睛疲劳，并且可能会被一些电子邮件客户自动翻转。

* 如果不支持深色模式，请提供可访问的回退样式。

**在深色模式环境中测试电子邮件**

* 使用Email Designer的[深色模式预览](#preview-dark-mode)，该预览使用反转的配色方案来提早发现问题。

* 使用[电子邮件渲染](../content-management/rendering.md)选项，该选项可利用Litmus在主要电子邮件客户端(Apple Mail、Gmail、Outlook)间模拟您的设计，并查看颜色和图像在深色模式下的行为。

<!--**Inline critical styles**

Inline CSS helps maintain more control over styling, as some clients strip external styles in dark mode.-->

## 支持深色模式的电子邮件客户端 {#supporting-email-clients}

以下是支持深色模式的主要电子邮件客户端列表。 但是，列出的电子邮件客户端的某些版本不支持深色模式，因此为了提高清晰度和准确性，也将在本表中列出这些版本。

>[!WARNING]
>
>深色模式的最终渲染取决于每个电子邮件客户端，因此结果可能因不同而异。 若要查看尽可能接近每个电子邮件客户端最终结果的模拟，请使用[电子邮件渲染](../content-management/rendering.md)选项。

| 支持深色模式的电子邮件客户端 | 兼容版本 | 不支持的版本 |
|---------|----------|---------|
| Apple Mail macOS | 12.4、16.0 | *10.3* |
| Apple Mail iOS | 13.0、16.1 | *12.2* |
| Outlook macOS | 2019， 16.70， 16.80 | NA |
| Outlook.com | 2019-07， 2022-12 | NA |
| Outlook iOS | 2020-01， 2022-12 | NA |
| Outlook Android | 2023-03 | *2020-01， 2022-12* |
| Samsung Email (Android) | 6.1 | *6.0* |
| Mozilla Thunderbird (macOS) | 68.4 | *60.8， 78.5， 91.13* |
| Fastmail（桌面Web邮件） | 2022-12 | *2021-07* |
| HEY（桌面Web邮件） | 2020-06 | *2022-12* |
| 橙色桌面Web邮件 | 2019-08,2021-03,2022-12,2024-04 | NA |
| 橙色iOS | 2022-12,2024-04 | *2020-01* |
| 橙色Android | 2024-04 | *2020-01， 2022-12* |
| LaPoste.net | 2021-08， 2022-12 | NA |
| SFR桌面Web邮件 | 2019-08， 2022-12 | NA |
| GMX(iOs和Android) | 2022-06 | NA |
| 1&amp;1(桌面Web邮件和Android) | 2022-06 | NA |
| WEB.DE(iOs和Android) | 2022-06 | NA |
| Free.fr | 2022-12 | NA |

<!--
* Check out the list of [email clients supporting dark mode](https://www.caniemail.com/search/?s=dark){target="_blank"}

* Learn more on Dark mode in this [Litmus blog post](https://www.litmus.com/blog/the-ultimate-guide-to-dark-mode-for-email-marketers){target="_blank"}
-->

## 电子邮件客户端不支持深色模式 {#non-supporting-email-clients}

某些电子邮件客户端允许用户将其界面切换到深色模式，但此设置不会影响HTML电子邮件的显示方式。 无论界面是处于浅色模式还是深色模式，您的电子邮件将呈现相同的形式。 以下是这些客户的列表：

| 电子邮件客户端不支持深色模式 |
|---------|
| Gmail(桌面Webmail、iOS、Android、Mobile Webmail) |
| Outlook Windows |
| Outlook Windows Mail |
| Yahoo！邮件 |
| AOL |
| 质子邮件 |
| SFR IOS |
| SFR ANDROID |
| GMX桌面网络邮件 |
| Mail.ru |
| WEB.DE桌面Web邮件 |
| T-online.de |
