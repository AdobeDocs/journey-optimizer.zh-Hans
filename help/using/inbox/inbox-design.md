---
title: 设计收件箱
description: 在Adobe Journey Optimizer中设计收件箱列表以及收件箱消息的扩展视图、模板和交互行为。
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 0ab71b21-0085-4a93-b319-3c960bd8f7dd
source-git-commit: 8ef401e6c92d94631f02762e4dc9ffab60657cb4
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# 设计收件箱 {#inbox-design}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;配置收件箱通道的布局、容量、未读指示器和空状态，以便消息按品牌呈现并可供读取，从而为目标用户档案在浅色和深色模式下提供清晰、一致的体验。

>[!ENDSHADEBOX]

收件箱设计控制如何将每封邮件呈现给收件箱界面中的目标用户档案。 该配置包括收件箱模板、列表和扩展的演示文稿，以及可区分新消息和已查看消息的读取状态指示器。

有关创建收件箱营销活动的完整过程，请参阅[创建收件箱](inbox-create.md)。

1. 打开您创建的[收件箱营销活动](inbox-create.md)的&#x200B;**[!UICONTROL 内容]**&#x200B;选项卡。

1. 设置&#x200B;**[!UICONTROL 容器标题]**。

1. 选择收件箱布局：

   * **[!UICONTROL 列表布局]**：在垂直列表中显示每个内容卡片，以便用户档案可以滚动浏览消息，并一次打开一个消息。

   * **[!UICONTROL 轮播布局]**：在水平轮播中显示卡片，以便配置文件可以在突出显示中滑动或横向移动而不离开收件箱表面。

   ![](assets/inbox-design-1.png)

1. 指定收件箱&#x200B;**容量**，即收件箱配置为容纳的内容卡片的最大数量。

1. 切换&#x200B;**[!UICONTROL 未读设置]**&#x200B;并配置未读消息的指示方式：

   * **[!UICONTROL 未读图标图像URL]**：提供显示在未读项目旁边或上的图像；添加深色模式URL，以便当应用程序或站点使用深色主题时，图标保持可见状态且品牌化。

   * **[!UICONTROL 背景颜色]**：设置浅色和（如果需要）深色模式的颜色，以使未读处理符合您的品牌并保留在收件箱背景的可读性。

   * **[!UICONTROL 版面]**：使用下拉菜单选择未读图标与版面对齐的位置。

   ![](assets/inbox-design-2.png)

1. 在&#x200B;**[!UICONTROL 空状态]**&#x200B;下，配置在没有可显示的消息时查看哪些用户档案：

   * **[!UICONTROL 消息文本]**：说明收件箱为空或建议下一步的简短文本。

   * **[!UICONTROL 图像URL]**：用于光模式的可选插图或图形，可加强空状态而不是显示空白区域。

   * **[!UICONTROL 深色图像URL]**：可选图像已针对深色模式进行了调整，因此空状态看起来是正确的，没有低对比度或边缘粗糙。

   ![](assets/inbox-design-3.png)

1. 单击![边栏图标](assets/do-not-localize/Smock_Rail_18_N.svg)以打开预览面板，并查看空收件箱的显示方式。

   ![](assets/inbox-design-3.png)

1. 在&#x200B;**[!UICONTROL 数据]**&#x200B;部分中，单击&#x200B;**[!UICONTROL 添加元]**&#x200B;以将自定义键/值对添加到有效负载。

1. 单击![](assets/do-not-localize/Smock_StarOutline_18_N.svg)图标以打开收件箱的深色模式预览，并确认您的深色主题颜色和图像。

   ![](assets/inbox-design-4.png)

准备就绪后，查看设置并激活收件箱。 激活后，您可以将其用于[内容卡](../content-card/create-content-card.md)。

