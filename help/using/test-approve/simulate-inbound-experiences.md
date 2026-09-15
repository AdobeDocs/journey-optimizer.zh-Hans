---
title: 模拟入站操作
description: 了解如何在激活之前在Action营销活动中模拟入站体验。
feature: Campaigns, Preview
topic: Content Management
role: User
level: Beginner
badge: label="Private Beta" type="Informative"
hide: true
exl-tag: PrivateBeta
source-git-commit: 916b5875a96eae7b0a4aca86fe35022f21841dd8
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 2%
---

# 模拟入站体验 {#simulate-inbound-experiences}

>[!BEGINSHADEBOX]

**在此页面上：**&#x200B;在模拟用户上线前验证入站操作促销活动体验，包括链接和二维预览、模拟行为和键限制。

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>此功能当前位于Private Beta中。 要请求访问权限，请与 Adobe 代表联系。

## 概述 {#inbound-simulation-overview}

入站体验模拟允许您在营销活动上线之前验证具有模拟用户的&#x200B;**操作营销活动**&#x200B;的个性化入站体验。 使用它可验证跨Web和移动预览路径的定位、决策、渲染的内容以及行为疑难解答。

模拟模式启动时，营销活动进入&#x200B;**[!UICONTROL 模拟]**&#x200B;状态。 您可以在模拟保持活动状态且活动内容和配置被锁定以进行编辑时离开并稍后返回（类似于已发布状态）。 模拟体验不会向生产受众公开。

有关完整的促销活动审核流程（包括内容预览和模拟上下文），请参阅[审核并激活操作促销活动](../campaigns/review-activate-campaign.md)。

## 进入并运行模拟模式 {#enter-simulation-mode}

要进入模拟模式，请执行以下操作：

1. 在操作营销活动中，访问&#x200B;**[!UICONTROL 查看以激活]**&#x200B;界面，然后选择&#x200B;**[!UICONTROL 模拟操作]**&#x200B;选项卡。

   ![](assets/simulation-mode-enter.png)

1. 使用以下可用方法之一选择要用于模拟的模拟用户：

   * **[!UICONTROL 浏览清单]** — 选择以前创建的模拟用户。
   * **[!UICONTROL 从表单创建]** — 按字段创建模拟用户字段。
   * **[!UICONTROL 从JSON创建]** — 导入JSON文件模拟用户配置文件有效负载。

   ![](assets/simulation-mode-ui.png)

   有关创建和管理模拟用户的更多详细信息，请参阅[创建和管理模拟用户](../building-journeys/simulate-journey.md#test-users)。

1. 选择或创建模拟用户后，这些用户将显示在中心窗格中。 对于每个用户，您可以查看详细信息、更新用户信息或从模拟列表中删除该用户。

   ![](assets/simulation-mode-users.png)

1. 若要为每个用户生成模拟输出，请单击&#x200B;**[!UICONTROL 生成链接]**&#x200B;按钮。 这将生成：

   * 用于预览所选用户呈现的入站体验的可共享URL。
   * 用于移动设备预览方案的二维码。

1. 对于每个模拟用户，请使用生成的控件来验证体验：

   ![](assets/simulation-mode-generate.png)

   | 按钮 | 作用 |
   | --- | --- |
   | ![打开链接按钮](assets/simulation-action-open.png) | 在浏览器中打开生成的链接，预览该模拟用户的集客体验。 |
   | ![复制链接按钮](assets/simulation-action-copy.png) | 复制生成的链接，以便共享该链接或将其粘贴到其他浏览器或设备中。 |
   | ![QR代码按钮](assets/simulation-action-qr.png) | 打开二维码（如果适用于该频道），选择&#x200B;**[!UICONTROL iOS]**&#x200B;或&#x200B;**[!UICONTROL Android]**，使用设备摄像头扫描该代码，然后在出现提示时输入显示的代码。 |
   | ![更多操作按钮](assets/simulation-action-more.png) | 打开&#x200B;**[!UICONTROL 打开保障会话]**&#x200B;或&#x200B;**[!UICONTROL 新保障会话]**&#x200B;的其他选项，并在Assurance用户界面中继续疑难解答。 |

1. 您可以随时退出模拟模式，方法是单击促销活动操作栏中的&#x200B;**[!UICONTROL 停止模拟]**，例如，如果您需要返回并编辑促销活动。
