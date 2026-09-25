---
solution: Journey Optimizer
product: journey optimizer
title: 个性化电子邮件背景
description: 了解如何对电子邮件背景进行个性化设置
feature: Email Design
topic: Content Management
role: User
level: Beginner, Intermediate
keywords: 背景，电子邮件，颜色，编辑器
exl-id: 09a2e892-8c6f-460d-8b12-5026582c6ed0
TQID: https://experienceleague.adobe.com/8kFppIm3Q-zHDqalE0Vt0CK5Z1ts9fGspVu476TapSk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
    internal-label: Content management
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
    internal-label: Email
subfeature_v2:
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
    internal-label: Email design
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
    internal-label: Publish
  - id: c41e8697-e629-4c38-96b3-564faaa17acf
    internal-label: Dynamic content
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
source-git-commit: 7047a27a870c50f7a093ec7d98d8398948b78edb
workflow-type: ht
source-wordcount: '887'
ht-degree: 100%
---
# 个性化电子邮件背景 {#backgrounds}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;了解如何在 Email Designer 中设置电子邮件正文、视口、结构和列级别的背景颜色和图像。

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ac_edition_backgroundimage"
>title="背景设置"
>abstract="您可以为自己的内容使用个性化的背景颜色或背景图像。 请注意，并非所有电子邮件客户端都支持背景图像。"

背景可帮助您强化品牌识别，并吸引收件人关注电子邮件中的关键区域。在电子邮件设计器中，您可以在内容的不同级别设置背景颜色或图像（从整体正文到单个结构和列），从而精确控制背景在电子邮件中的渲染方式。

在电子邮件设计器中设置背景时，请牢记以下最佳做法：

* 仅当您的设计需要背景颜色时，才对正文应用背景颜色。
* 尽可能在列级别设置背景颜色。
* 避免在图像或文本组件上使用背景颜色，因为它们更难于管理。
* 发送前，请在实际邮件客户端中测试背景图像，因为渲染效果可能与电子邮件设计器预览不一致。

以下设置允许您在电子邮件内容的任意级别应用背景颜色或图像，从正文一直到单个结构和列。

>[!TIP]
>
>如果向电子邮件应用了主题，则无法直接覆盖主题为特定组件设置的背景颜色。必须先使用&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡中的专用图标解锁该样式。[了解如何操作](apply-email-themes.md#unlocking-styles)

## 设置背景颜色 {#background-color}

1. **正文背景颜色** – 设置整封电子邮件的&#x200B;**[!UICONTROL 背景颜色]**。请确保在&#x200B;**[!UICONTROL 导航树]**（可从左侧调色板访问）中选择&#x200B;**[!UICONTROL 正文]**，并使用右侧的&#x200B;**[!UICONTROL 样式]**&#x200B;选项卡中的专用选项。

   ![电子邮件设计器界面，其中显示在导航树中选择了“正文”，且在“样式”面板中突出显示了“背景颜色”选项](assets/background_1.png)

1. **视口背景颜色** – 设置&#x200B;**[!UICONTROL 视口颜色]**，以便独立于正文背景颜色，为所有结构组件应用相同的背景颜色。

   ![电子邮件设计器的“样式”面板界面，其中突出显示了“视口颜色”选项，并打开了拾色器，以便选择要应用于所有结构的背景颜色](assets/background_2.png)

1. **结构背景颜色** – 要将背景颜色应用于单个结构组件，请直接在画布中或从左侧调色板中选择它，然后为该结构设置特定颜色。

   ![电子邮件设计器的“样式”面板界面，其中有一个结构被选中，并且突出显示了“背景颜色”选项](assets/background_3.png)

   >[!TIP]
   >
   >在这种情况下，切勿设置视口背景颜色，因为它可能会隐藏结构背景颜色。

1. **列背景颜色** – 在列级别设置背景颜色。同样，请确保从左侧面板中选择所需的列，并设置该列的特定颜色。

   ![电子邮件设计器的“样式”面板界面，其中一个列被选中，并且突出显示了“背景颜色”选项](assets/background_5.png)

   >[!TIP]
   >
   >这是最常见的用例和最佳做法，因为它能让您在编辑电子邮件的其余部分时拥有更大的灵活性。

## 设置背景图像 {#background-image}

您还可以为结构或列组件的内容设置&#x200B;**[!UICONTROL 背景图像]**。这最常在结构级别使用；在列级别设置一个也是可行的，但很少使用。

>[!NOTE]
>
>某些电子邮件程序不支持背景图像。 如果不支持，将改用行背景颜色。 请务必选择合适的备用背景颜色，以防图像无法显示。

![电子邮件设计器的“样式”面板，其中“背景图像”处于启用状态，并且“图像放置环境”被设置为“全高 – 右侧”，显示图像填满某一列](assets/background_4.png)

>[!TIP]
>
>发送前，请在实际的电子邮件客户端中预览背景图像，不要只在电子邮件设计器中查看预览效果。相同的图像和放置环境可以在编辑器中正确渲染，但在某些客户端中（例如 iOS 上的 Outlook）会被以不同的方式拉伸或裁切。

设置背景图像后，使用&#x200B;**[!UICONTROL 图像放置环境]**&#x200B;下拉菜单控制图像在结构或列中的填充方式。以下选项可供选择：

![电子邮件设计器的“样式”面板界面，其中显示“图片放置环境”下拉菜单及各种选项。](assets/background_6.png){width=80%}

**缩放以填充，居中：**

* **[!UICONTROL 适合]** – 将图像沿两个坐标轴拉伸以填满容器，不保留其纵横比。
* **[!UICONTROL 全宽]** – 根据容器宽度按比例缩放图像，并使其垂直居中。
* **[!UICONTROL 全高]** – 根据容器高度按比例缩放图像，并使其水平居中。

**缩放以填充，锚定到边缘：**

* **[!UICONTROL 全宽 – 顶部]** – 与&#x200B;**[!UICONTROL 全宽]**&#x200B;相同，但锚定到容器顶部。溢出的部分在底部被裁剪。
* **[!UICONTROL 全宽 – 底部]** – 与&#x200B;**[!UICONTROL 全宽]**&#x200B;相同，但锚定到容器底部。溢出的部分在顶部被裁剪。
* **[!UICONTROL 全高 – 左侧]** – 与&#x200B;**[!UICONTROL 全高]**&#x200B;相同，但锚定到容器左侧。溢出的部分在右侧被裁剪。
* **[!UICONTROL 全高 – 右侧]** – 与&#x200B;**[!UICONTROL 全高]**&#x200B;相同，但锚定到容器右侧。溢出的部分在左侧被裁剪。

**平铺：**

* **[!UICONTROL 重复]** – 以原始大小平铺图像，填满容器。

**定位（不缩放）：**

* **[!UICONTROL 左]**、**[!UICONTROL 右]**、**[!UICONTROL 中]**、**[!UICONTROL 上]**、**[!UICONTROL 下]** – 以原始大小定位图像，并将其锚定到容器的相应边缘或中心。

>[!NOTE]
>
>当图像与结构比例不匹配时，与上方的居中选项相比，边缘锚定选项可让您更好地控制图像的哪一部分保持可见。

{{$include /help/_includes/do-not-localize/email/ai-augmented-backgrounds.md}}
