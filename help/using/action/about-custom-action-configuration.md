---
solution: Journey Orchestration
title: 关于自定义操作配置
description: 了解如何配置自定义操作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: a174944bb8efcb67d758d4fe215674c1b8bbee13
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 6%

---

# 配置操作 {#configure-an-action}

如果您使用第三方系统来发送消息，或者如果您希望历程将API调用发送到第三方系统，则可以在此处配置其与历程的连接。 然后，技术用户定义的自定义操作将在历程左侧面板的&#x200B;**[!UICONTROL Action]**&#x200B;类别中可用（请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)）。 以下是可通过自定义操作连接到的一些系统示例：Epsilon、Facebook、Adobe.io、Firebase等

[此页面](../limitations.md)中列出了限制。

您可以使用自定义操作动态传递收藏集。 请参见此[用例](../limitations.md)。

以下是配置自定义操作所需的主要步骤：

1. 在“管理”菜单部分，选择&#x200B;**[!UICONTROL Configurations]**。 在&#x200B;**[!UICONTROL Actions]**&#x200B;部分中，单击&#x200B;**[!UICONTROL Manage]**。 单击&#x200B;**[!UICONTROL Create Action]**&#x200B;以创建新操作。 操作配置窗格将在屏幕右侧打开。

   ![](../assets/custom2.png)

1. 输入操作的名称。

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 向操作添加描述。 此步骤是可选的。
1. 使用此操作的历程数显示在&#x200B;**[!UICONTROL Used in]**&#x200B;字段中。 您可以单击&#x200B;**[!UICONTROL View journeys]**&#x200B;按钮以显示使用此操作的历程列表。
1. 定义不同的&#x200B;**[!UICONTROL URL Configuration]**&#x200B;参数。 请参阅[此页](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置&#x200B;**[!UICONTROL Authentication]**&#x200B;部分。 此配置与数据源的配置相同。  请参阅[此小节](../datasource/external-data-sources.md#section_wjp_nl5_nhb)。
1. 定义&#x200B;**[!UICONTROL Action parameters]**。 请参阅[此页](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 单击 **[!UICONTROL Save]**。

   自定义操作现已配置完成，可随时用于您的历程。 请参阅[此页](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在历程中使用自定义操作时，大多数参数都是只读的。 您只能修改&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Description]**、**[!UICONTROL URL]**&#x200B;字段和&#x200B;**[!UICONTROL Authentication]**&#x200B;部分。

## URL 配置 {#url-configuration}

配置自定义操作时，您需要定义以下&#x200B;**[!UICONTROL URL Configuration]**&#x200B;参数：

![](../assets/journeyurlconfiguration.png)

1. 在&#x200B;**[!UICONTROL URL]**&#x200B;字段中，指定外部服务的URL:

   * 如果URL是静态的，请在此字段中输入URL。

   * 如果URL包含动态路径，则只输入URL的静态部分，即方案、主机、端口，以及（可选）路径的静态部分。

      示例: `https://xxx.yyy.com/somethingstatic/`

      在将自定义操作添加到历程时，您将指定URL的动态路径。 [了解详情](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >出于安全原因，我们强烈建议您对URL使用HTTPS方案。 我们不允许使用非公共的Adobe地址和IP地址。
   >
   >定义自定义操作时仅允许使用默认端口：80表示http，443表示https。

1. 选择&#x200B;**[!UICONTROL Method]**&#x200B;调用：它可以是&#x200B;**[!UICONTROL POST]**&#x200B;或&#x200B;**[!UICONTROL PUT]**。
1. 在&#x200B;**[!UICONTROL Headers]**&#x200B;部分中，定义要发送到外部服务的请求消息的HTTP标头：
   1. 要添加标题字段，请单击&#x200B;**[!UICONTROL Add a header field]**。
   1. 输入标题字段的键。
   1. 要为键值对设置动态值，请选择&#x200B;**[!UICONTROL Variable]**。 否则，请选择&#x200B;**[!UICONTROL Constant]**。

      例如，对于时间戳，您可以设置动态值。

   1. 如果已选择&#x200B;**[!UICONTROL Constant]**，则输入常数值。

      如果已选择&#x200B;**[!UICONTROL Variable]**，则在将自定义操作添加到历程时将指定此变量。 [了解详情](../building-journeys/using-custom-actions.md)。

      ![](../assets/journeyurlconfiguration2.png)

   1. 要删除标题字段，请指向标题字段，然后单击&#x200B;**[!UICONTROL Delete]**&#x200B;图标。
   默认情况下，将设置&#x200B;**[!UICONTROL Content-Type]**&#x200B;和&#x200B;**[!UICONTROL Charset]**&#x200B;标头字段。 您无法修改或删除这些字段。

   在将自定义操作添加到历程后，如果历程处于草稿状态，您仍可以向该历程添加标题字段。 如果您不希望历程受配置更改的影响，请复制自定义操作并将标题字段添加到新的自定义操作。

   >[!NOTE]
   >
   >将根据字段解析规则验证标头。 [了解详情](https://tools.ietf.org/html/rfc7230#section-3.2.4)。

## 定义操作参数 {#define-the-message-parameters}

![](../assets/messageparameterssection.png)

在&#x200B;**[!UICONTROL Action parameters]**&#x200B;部分中，粘贴要发送到外部服务的JSON有效负载示例。

![](../assets/customactionpayloadmessage.png)

>[!NOTE]
>
>有效负载中的字段名称不能包含“。” 字符. 不能以“$”字符开头。

您将能够定义参数类型(例如：字符串、整数等)。

您还可以选择指定参数是常量还是变量：

* 常量表示参数的值由技术人员在操作配置窗格中定义。 跨历程的值将始终相同。 在历程中使用自定义操作时，它不会有所不同，营销人员也不会看到它。 例如，它可能是第三方系统所需的ID。 在这种情况下，切换常量/变量右侧的字段是传递的值。
* 变量表示参数的值会有所不同。 在历程中使用此自定义操作的营销人员可以自由地传递他们想要的值，或指定在何处检索此参数的值(例如，从事件、从Adobe Experience Platform等)。 在这种情况下，切换常量/变量右侧的字段是营销人员在命名此参数的历程中看到的标签。

![](../assets/customactionpayloadmessage2.png)

