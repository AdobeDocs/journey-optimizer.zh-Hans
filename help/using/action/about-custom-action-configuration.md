---
solution: Journey Optimizer
title: 配置自定义操作
description: 了解如何配置自定义操作
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: f1ac47a0cb405eaadc5428e7e5479eaf776d7abe
workflow-type: tm+mt
source-wordcount: '922'
ht-degree: 6%

---

# 配置自定义操作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自定义操作"
>abstract="如果您使用第三方系统发送消息，或者如果您希望历程将API调用发送到第三方系统，请使用自定义操作配置其与历程的连接。 例如，您可以通过自定义操作连接到以下系统：Epsilon，Slack, [Adobe开发人员](https://developer.adobe.com)、Firebase等"

如果您使用第三方系统发送消息，或者如果您希望历程将API调用发送到第三方系统，请使用自定义操作配置其与历程的连接。 例如，您可以通过自定义操作连接到以下系统：Epsilon，Slack, [Adobe开发人员](https://developer.adobe.com){target=&quot;_blank&quot;}、Firebase等。

自定义操作是技术用户定义并可供营销人员使用的其他操作。 配置完毕后，这些组件会显示在历程的左侧面板(位于 **[!UICONTROL Action]** 类别。 请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

## 限制{#custom-actions-limitations}

自定义操作在 [本页](../start/limitations.md).

在自定义操作参数中，您可以传递简单的集合以及对象集合。 进一步了解 [本页](../building-journeys/collections.md#limitations).

另请注意，自定义操作参数具有预期的格式(例如：字符串、小数等)。 您必须谨慎遵循这些预期格式。 在中了解详情 [用例](../building-journeys/collections.md).


## 配置步骤 {#configuration-steps}

以下是配置自定义操作所需的主要步骤：

1. 在“管理”菜单部分，选择 **[!UICONTROL Configurations]**. 在  **[!UICONTROL Actions]** ，单击 **[!UICONTROL Manage]**. 单击 **[!UICONTROL Create Action]** 创建新操作。 操作配置窗格将在屏幕右侧打开。

   ![](assets/custom2.png)

1. 输入操作的名称。

   >[!NOTE]
   >
   >请勿使用空格或特殊字符。请勿使用超过 30 个字符。

1. 向操作添加描述。 此步骤是可选的。
1. 使用此操作的历程数显示在 **[!UICONTROL Used in]** 字段。 您可以单击 **[!UICONTROL View journeys]** 按钮以显示使用此操作的历程列表。
1. 定义不同的 **[!UICONTROL URL Configuration]** 参数。 请参阅[此页](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置 **[!UICONTROL Authentication]** 中。 此配置与数据源的配置相同。  请参阅[此小节](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定义 **[!UICONTROL Action parameters]**. 请参阅[此页](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 单击 **[!UICONTROL Save]**。

   自定义操作现已配置完成，可随时用于您的历程。 请参阅[此页](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在历程中使用自定义操作时，大多数参数都是只读的。 您只能修改 **[!UICONTROL Name]**, **[!UICONTROL Description]**, **[!UICONTROL URL]** 字段和 **[!UICONTROL Authentication]** 中。

## URL 配置 {#url-configuration}

配置自定义操作时，您需要定义以下内容 **[!UICONTROL URL Configuration]** 参数：

![](assets/journeyurlconfiguration.png)

1. 在 **[!UICONTROL URL]** 字段中，指定外部服务的URL:

   * 如果URL是静态的，请在此字段中输入URL。

   * 如果URL包含动态路径，则只输入URL的静态部分，即方案、主机、端口，以及（可选）路径的静态部分。

      示例: `https://xxx.yyy.com/somethingstatic/`

      在将自定义操作添加到历程时，您将指定URL的动态路径。 [了解详情](../building-journeys/using-custom-actions.md)。
   >[!NOTE]
   >
   >出于安全原因，我们强烈建议您对URL使用HTTPS方案。 我们不允许使用非公共的Adobe地址和IP地址。
   >
   >定义自定义操作时仅允许使用默认端口：80表示http，443表示https。

1. 选择调用 **[!UICONTROL Method]**:它可以 **[!UICONTROL POST]** 或 **[!UICONTROL PUT]**.
1. 在 **[!UICONTROL Headers]** 部分，定义要发送到外部服务的请求消息的HTTP标头：
   1. 要添加标题字段，请单击 **[!UICONTROL Add a header field]**.
   1. 输入标题字段的键。
   1. 要为键值对设置动态值，请选择 **[!UICONTROL Variable]**. 否则，请选择 **[!UICONTROL Constant]**.

      例如，对于时间戳，您可以设置动态值。

   1. 如果已选择 **[!UICONTROL Constant]**，然后输入常数值。

      如果已选择 **[!UICONTROL Variable]**，则在将自定义操作添加到历程时，将指定此变量。 [了解详情](../building-journeys/using-custom-actions.md)。

      ![](assets/journeyurlconfiguration2.png)

   1. 要删除标题字段，请指向标题字段，然后单击 **[!UICONTROL Delete]** 图标。
   的 **[!UICONTROL Content-Type]** 和 **[!UICONTROL Charset]** 标题字段默认设置。 您无法修改或删除这些字段。

   在将自定义操作添加到历程后，如果历程处于草稿状态，您仍可以向该历程添加标题字段。 如果您不希望历程受配置更改的影响，请复制自定义操作并将标题字段添加到新的自定义操作。

   >[!NOTE]
   >
   >将根据字段解析规则验证标头。 [了解详情](https://tools.ietf.org/html/rfc7230#section-3.2.4)。

## 定义操作参数 {#define-the-message-parameters}

![](assets/messageparameterssection.png)

在 **[!UICONTROL Action parameters]** 部分，粘贴要发送到外部服务的JSON有效负载示例。

![](assets/customactionpayloadmessage.png)

>[!NOTE]
>
>有效负载中的字段名称不能包含“。” 字符. 不能以“$”字符开头。

您将能够定义参数类型(例如：字符串、整数等)。

您还可以选择指定参数是常量还是变量：

* 常量表示参数的值由技术人员在操作配置窗格中定义。 跨历程的值将始终相同。 在历程中使用自定义操作时，它不会有所不同，营销人员也不会看到它。 例如，它可能是第三方系统所需的ID。 在这种情况下，切换常量/变量右侧的字段是传递的值。
* 变量表示参数的值会有所不同。 在历程中使用此自定义操作的营销人员可以自由地传递他们想要的值，或指定在何处检索此参数的值(例如，从事件、从Adobe Experience Platform等)。 在这种情况下，切换常量/变量右侧的字段是营销人员在命名此参数的历程中看到的标签。

![](assets/customactionpayloadmessage2.png)
