---
title: 在Journey Optimizer中创建应用程序内通知
description: 了解如何在Journey Optimizer中创建应用程序内消息
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: 应用程序内、消息、创建、入门
exl-id: b3b79fe2-7db3-490d-9c3d-87267aa55eea
source-git-commit: 47185cdcfb243d7cb3becd861fec87abcef1f929
workflow-type: tm+mt
source-wordcount: '2009'
ht-degree: 12%

---

# 创建应用程序内消息 {#create-in-app}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_inapp_triggers"
>title="管理应用程序内触发器"
>abstract="通过选择将激活消息的特定事件和标准，有效地控制触发器。利用规则生成器，用户可以定义精确的条件和值。当满足这些条件时，他们将启动一系列操作，包括投放应用程序内消息。"

您可以在营销活动或历程中添加应用程序内消息。 请按照下面详述的步骤在两个上下文中创建应用程序内消息。

请注意，应用程序内消息不受用户在操作系统上选择加入或选择退出推送通知的影响。

>[!BEGINTABS]

>[!TAB 向历程添加应用程序内消息]

要在历程中添加应用程序内消息，请执行以下步骤：

1. 打开您的历程，然后从面板的&#x200B;**[!UICONTROL 操作]**&#x200B;部分拖放&#x200B;**[!UICONTROL 应用程序内]**&#x200B;活动。

   当用户档案到达其历程结尾时，显示给他们的任何应用程序内消息都将自动过期。 因此，会在应用程序内活动后自动添加等待活动，以确保计时正确。

   ![](assets/in_app_journey_1.png)

1. 为您的消息输入&#x200B;**[!UICONTROL 标签]**&#x200B;和&#x200B;**[!UICONTROL 描述]**。

1. 选择要使用的[应用程序内配置](inapp-configuration.md#channel-prerequisites)。

   ![](assets/in_app_journey_2.png)

1. 您现在可以使用&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计内容。 [了解详情](design-in-app.md)

1. 单击&#x200B;**[!UICONTROL 编辑触发器]**&#x200B;以选择将触发消息的事件和条件。 规则构建器使用户能够指定标准和值，这些标准和值在满足时触发一组操作，如发送应用程序内消息。

   ![](assets/in_app_journey_4.png)

   1. 如果需要，单击事件下拉列表以更改触发器。

      +++请参阅可用的触发器。

      | 包 | 触发器 | 定义 |
      |---|---|---|
      | 将数据发送到Platform | 将数据发送到Platform | 在移动设备应用程序发出边缘体验事件以将数据发送到Adobe Experience Platform时触发。 API通常会从AEP Edge扩展调用[sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent)。 |
      | 核心跟踪 | 跟踪操作 | 在调用移动设备代码API [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)中提供的旧版功能时触发。 |
      | 核心跟踪 | 跟踪状态 | 在调用移动设备代码API [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate)中提供的旧版功能时触发。 |
      | 核心跟踪 | 收集PII | 在调用移动设备代码API [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii)中提供的旧版功能时触发。 |
      | 应用程序生命周期 | 应用程序启动 | 在每次运行时触发，包括崩溃次数和安装次数。在超出生命周期会话超时后，当从背景恢复应用程序时也会触发。 |
      | 应用程序生命周期 | 应用程序安装 | 安装或重新安装后，在首次运行时触发。 |
      | 应用程序生命周期 | 应用程序更新 | 升级后或版本号变更后，在首次运行时触发。 |
      | 应用程序生命周期 | 应用程序关闭 | 在应用程序关闭时触发。 |
      | 应用程序生命周期 | 应用程序崩溃 | 当应用程序在关闭前未转入背景时触发。当应用程序在崩溃后启动时会发送该事件。 Adobe Mobile 崩溃报告不实施全局未捕获异常处理程序。 |
      | Places | 输入POI | 在您的客户进入您配置的目标点(POI)时，由Places SDK触发。 |
      | Places | 退出POI | 在您的客户退出您配置的目标点(POI)时，由Places SDK触发。 |

+++

   1. 如果希望触发器考虑多个事件或条件，请单击&#x200B;**[!UICONTROL 添加条件]**。

   1. 如果要添加更多&#x200B;**[!UICONTROL 触发器]**，请选择&#x200B;**[!UICONTROL 或]**&#x200B;条件以进一步扩展规则。

      ![](assets/in_app_create_3.png)

   1. 如果要添加&#x200B;**[!UICONTROL 特征]**&#x200B;并更好地优化规则，请选择&#x200B;**[!UICONTROL 和]**&#x200B;条件。

      +++查看可用的特征。

      | 包 | 特征 | 定义 |
      |---|---|---|
      | 设备信息 | 运营商名称 | 当满足列表中的运营商名称之一时触发。 |
      | 设备信息 | 设备名称 | 当满足设备名称之一时触发。 |
      | 设备信息 | 区域设置 | 当满足列表中的一种语言时触发。 |
      | 设备信息 | 操作系统版本 | 当满足指定的操作系统版本之一时触发。 |
      | 设备信息 | 以前的操作系统版本 | 当满足指定的先前操作系统版本之一时触发。 |
      | 设备信息 | 运行模式 | 如果运行模式为应用程序或扩展，则会触发。 |
      | 应用程序生命周期 | 应用程序 ID | 当满足指定的应用程序ID时触发。 |
      | 应用程序生命周期 | Day of week | 当满足一周中的指定日期时触发。 |
      | 应用程序生命周期 | 首次使用后间隔天数 | 当满足自首次使用以来的指定天数时触发。 |
      | 应用程序生命周期 | 上次使用后间隔天数 | 当满足自上次使用后指定的天数时触发。 |
      | 应用程序生命周期 | 升级后间隔天数 | 当满足自上次升级以来的指定天数时触发。 |
      | 应用程序生命周期 | 安装日期 | 当满足指定的安装日期时触发。 |
      | 应用程序生命周期 | 启动次数 | 当满足指定的启动次数时触发。 |
      | 应用程序生命周期 | 时间 | 当满足指定的时间时触发。 |
      | Places | 当前POI | 在您的客户进入指定的目标点(POI)时，由Places SDK触发。 |
      | Places | 上次进入的POI | 根据您客户上次进入的目标点(POI)，由Places SDK触发。 |
      | Places | 上次退出的POI | 根据您的客户上次退出兴趣点(POI)，由Places SDK触发。 |

+++

      ![](assets/in_app_create_8.png)

   1. 单击“**[!UICONTROL 创建组]**”将触发器组合在一起。

      ![](assets/in_app_journey_3.png)

   1. 选择应用程序内消息处于活动状态时触发的频率：

      * **[!UICONTROL 每次都显示]**：当在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中发生选定的事件时，始终显示消息。
      * **[!UICONTROL 显示一次]**：仅在首次在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中出现选定的事件时显示此消息。
      * **[!UICONTROL 显示直至点进次数]**：在SDK发送交互事件并执行“已点击”操作之前，出现在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中选择的事件时显示此消息。

1. 如有必要，请通过拖放其他操作或事件来完成旅程流程。 [了解详情](../building-journeys/about-journey-activities.md)

1. 应用程序内消息就绪后，完成配置并发布历程以激活它。

有关如何配置历程的详细信息，请参阅[此页面](../building-journeys/journey-gs.md)。

>[!TAB 向营销活动添加应用程序内消息]

要在营销策划中添加应用程序内消息，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 营销活动]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 创建营销活动]**。

1. 选择要执行的营销活动类型

   * **已计划 — 营销**：立即或在指定日期执行营销活动。 计划的营销活动旨在发送营销消息。 它们从用户界面配置和执行。

   * **API触发 — 营销/事务性**：使用API调用执行营销活动。 API触发的营销活动旨在发送营销或事务型消息，即，在个人执行操作（密码重置、购物车购买等）之后发送的消息。

1. 从&#x200B;**[!UICONTROL 属性]**&#x200B;部分，输入&#x200B;**[!UICONTROL 标题]**&#x200B;和&#x200B;**[!UICONTROL 描述]**&#x200B;描述。

1. 要将自定义或核心数据使用标签分配给应用程序内消息，请选择&#x200B;**[!UICONTROL 管理访问权限]**。 [了解详情](../administration/object-based-access.md)。

1. 单击&#x200B;**[!UICONTROL 选择受众]**&#x200B;按钮，从可用Adobe Experience Platform受众列表中定义要定位的受众。 [了解详情](../audience/about-audiences.md)。

   ![](assets/in_app_create_2.png)

1. 在&#x200B;**[!UICONTROL 身份命名空间]**&#x200B;字段中，选择要使用的命名空间，以便识别所选受众中的个人。 [了解详情](../event/about-creating.md#select-the-namespace)。

1. 在&#x200B;**[!UICONTROL 操作]**&#x200B;部分中，选择&#x200B;**[!UICONTROL 应用程序内消息]**，然后选择或创建新配置。

   在[此页面](inapp-configuration.md)上了解有关应用程序内配置的更多信息。

   ![](assets/in_app_create_1.png)

1. 单击&#x200B;**[!UICONTROL 创建试验]**&#x200B;开始配置内容试验并创建处理以测量其性能并为目标受众确定最佳选项。 [了解详情](../content-management/content-experiment.md)

1. 单击&#x200B;**[!UICONTROL 编辑触发器]**&#x200B;以选择将触发消息的事件和条件。 规则构建器使用户能够指定标准和值，这些标准和值在满足时触发一组操作，如发送应用程序内消息。

   1. 如果需要，单击事件下拉列表以更改触发器。

      +++请参阅可用的触发器。

      | 包 | 触发器 | 定义 |
      |---|---|---|
      | 将数据发送到Platform | 将数据发送到Platform | 在移动设备应用程序发出边缘体验事件以将数据发送到Adobe Experience Platform时触发。 API通常会从AEP Edge扩展调用[sendEvent](https://developer.adobe.com/client-sdks/documentation/edge-network/api-reference/#sendevent)。 |
      | 核心跟踪 | 跟踪操作 | 在调用移动设备代码API [trackAction](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackaction)中提供的旧版功能时触发。 |
      | 核心跟踪 | 跟踪状态 | 在调用移动设备代码API [trackState](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#trackstate)中提供的旧版功能时触发。 |
      | 核心跟踪 | 收集PII | 在调用移动设备代码API [collectPII](https://developer.adobe.com/client-sdks/documentation/mobile-core/api-reference/#collectpii)中提供的旧版功能时触发。 |
      | 应用程序生命周期 | 应用程序启动 | 在每次运行时触发，包括崩溃次数和安装次数。在超出生命周期会话超时后，当从背景恢复应用程序时也会触发。 |
      | 应用程序生命周期 | 应用程序安装 | 安装或重新安装后，在首次运行时触发。 |
      | 应用程序生命周期 | 应用程序更新 | 升级后或版本号变更后，在首次运行时触发。 |
      | 应用程序生命周期 | 应用程序关闭 | 在应用程序关闭时触发。 |
      | 应用程序生命周期 | 应用程序崩溃 | 当应用程序在关闭前未转入背景时触发。当应用程序在崩溃后启动时会发送该事件。 Adobe Mobile 崩溃报告不实施全局未捕获异常处理程序。 |
      | Places | 输入POI | 在您的客户进入您配置的目标点(POI)时，由Places SDK触发。 |
      | Places | 退出POI | 在您的客户退出您配置的目标点(POI)时，由Places SDK触发。 |

+++

   1. 如果希望触发器考虑多个事件或条件，请单击&#x200B;**[!UICONTROL 添加条件]**。

   1. 如果要添加更多&#x200B;**[!UICONTROL 触发器]**，请选择&#x200B;**[!UICONTROL 或]**&#x200B;条件以进一步扩展规则。

      ![](assets/in_app_create_3.png)

   1. 如果要添加&#x200B;**[!UICONTROL 特征]**&#x200B;并更好地优化规则，请选择&#x200B;**[!UICONTROL 和]**&#x200B;条件。

      +++查看可用的特征。

      | 包 | 特征 | 定义 |
      |---|---|---|
      | 设备信息 | 运营商名称 | 当满足列表中的运营商名称之一时触发。 |
      | 设备信息 | 设备名称 | 当满足设备名称之一时触发。 |
      | 设备信息 | 区域设置 | 当满足列表中的一种语言时触发。 |
      | 设备信息 | 操作系统版本 | 当满足指定的操作系统版本之一时触发。 |
      | 设备信息 | 以前的操作系统版本 | 当满足指定的先前操作系统版本之一时触发。 |
      | 设备信息 | 运行模式 | 如果运行模式为应用程序或扩展，则会触发。 |
      | 应用程序生命周期 | 应用程序 ID | 当满足指定的应用程序ID时触发。 |
      | 应用程序生命周期 | Day of week | 当满足一周中的指定日期时触发。 |
      | 应用程序生命周期 | 首次使用后间隔天数 | 当满足自首次使用以来的指定天数时触发。 |
      | 应用程序生命周期 | 上次使用后间隔天数 | 当满足自上次使用后指定的天数时触发。 |
      | 应用程序生命周期 | 升级后间隔天数 | 当满足自上次升级以来的指定天数时触发。 |
      | 应用程序生命周期 | 安装日期 | 当满足指定的安装日期时触发。 |
      | 应用程序生命周期 | 启动次数 | 当满足指定的启动次数时触发。 |
      | 应用程序生命周期 | 时间 | 当满足指定的时间时触发。 |
      | Places | 当前POI | 在您的客户进入指定的目标点(POI)时，由Places SDK触发。 |
      | Places | 上次进入的POI | 根据您客户上次进入的目标点(POI)，由Places SDK触发。 |
      | Places | 上次退出的POI | 根据您的客户上次退出兴趣点(POI)，由Places SDK触发。 |

+++

      ![](assets/in_app_create_8.png)

   1. 单击“**[!UICONTROL 创建组]**”将触发器组合在一起。

1. 选择应用程序内消息处于活动状态时触发的频率。 可以使用以下选项：

   * **[!UICONTROL Everytime]**：当在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中选定的事件发生时，始终显示消息。
   * **[!UICONTROL 一次]**：仅在首次在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中发生选定的事件时显示此消息。
   * **[!UICONTROL 点进之前]**：当在&#x200B;**[!UICONTROL 移动设备应用程序触发器]**&#x200B;下拉列表中选择的事件发生时，显示此消息，直到SDK发送了一个交互事件，并且执行了“已点击”操作。
   * **[!UICONTROL X次]**：显示此消息X次。

1. 如果需要，请选择在一周中哪一天&#x200B;]**或哪一天**[!UICONTROL &#x200B;时间&#x200B;]**显示应用程序内消息。**[!UICONTROL 

1. 营销活动旨在按特定日期或循环频率执行。 在[本节](../campaigns/create-campaign.md#schedule)中了解如何配置促销活动的&#x200B;**[!UICONTROL 计划]**。

   ![](assets/in-app-schedule.png)

1. 您现在可以使用&#x200B;**[!UICONTROL 编辑内容]**&#x200B;按钮开始设计内容。 [了解详情](design-in-app.md)

   ![](assets/in_app_create_4.png)

>[!ENDTABS]

## 操作说明视频{#video}

* 以下视频介绍了如何在营销活动中创建、配置和发布应用程序内消息。

  +++观看视频

  >[!VIDEO](https://video.tv.adobe.com/v/3410430?quality=12&learn=on)

+++

* 以下视频介绍了如何配置和分析A/B测试应用程序内消息的内容实验。

  +++观看视频

  >[!VIDEO](https://video.tv.adobe.com/v/3419898/?learn=on&autoplay=true)

+++

* 以下视频介绍如何在历程中创建应用程序内消息以及如何测试和发布历程。

  +++观看视频

  >[!VIDEO](https://video.tv.adobe.com/v/3423077/?learn=on&autoplay=true)

+++

**相关主题：**

* [设计应用程序内消息](design-in-app.md)
* [测试并发送应用程序内消息](send-in-app.md)
* [应用程序内报告](../reports/campaign-global-report-cja-inapp.md)
* [应用程序内配置](inapp-configuration.md)