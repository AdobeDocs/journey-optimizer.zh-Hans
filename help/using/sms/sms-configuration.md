---
solution: Journey Optimizer
product: journey optimizer
title: 配置短信渠道
description: 了解如何配置环境以使用Journey Optimizer发送短信
role: Admin
level: Intermediate
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: 442e3213ad512b62332cd08d6639dfc52bdc766a
workflow-type: tm+mt
source-wordcount: '920'
ht-degree: 18%

---

# 配置短信渠道 {#sms-configuration}

[!DNL Journey Optimizer] 允许您创建历程并向目标受众发送消息。

在发送短信之前，请配置您的实例。 您需要 [集成提供程序设置](#create-api) 使用Journey Optimizer和 [创建短信表面](#message-preset-sms) （即短信预设）。 这些步骤必须由 [Adobe Journey Optimizer 系统管理员](../start/path/administrator.md)执行。

## 先决条件{#sms-prerequisites}

Adobe Journey Optimizer目前与Sinch和Twilio等第三方提供商集成，这些提供商提供独立于Adobe Journey Optimizer的短信服务。

在配置SMS之前，您必须使用这些SMS提供商之一创建一个帐户，以接收API令牌和服务ID，从而能够在Adobe Journey Optimizer和适用的SMS提供商之间建立连接。

您对短信服务的使用将受适用短信提供商提供的其他条款和条件的约束。 鉴于Sinch和Twilio是第三方产品，可供Adobe Journey Optimizer用户通过集成使用任何与短信服务相关的问题或查询，Sinch或Twilio的用户需要联系适用的短信提供商寻求帮助。 Adobe不控制第三方产品，也不对第三方产品负责。

>[!CAUTION]
>
>要访问和编辑SMS子域，您必须具有 **[!UICONTROL 管理短信子域]** 生产沙盒的权限。

## 创建新的API凭据 {#create-api}

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api_header"
>title="使用 Journey Optimizer 配置短信供应商"
>abstract="选择您的供应商并填写短信 API 凭据。"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_api"
>title="使用 Journey Optimizer 配置短信供应商"
>abstract="在发送短信之前，您必须将供应商设置与 Journey Optimizer 集成。完成后，您将需要创建一个短信表面。这些步骤必须由 Adobe Journey Optimizer 系统管理员执行。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/sms/sms-configuration.html#message-preset-sms" text="创建短信渠道表面"

>[!CONTEXTUALHELP]
>id="ajo_admin_sms_configuration"
>title="选择短信供应商配置"
>abstract="选择为您的短信供应商配置的 API 凭据。"

要使用Journey Optimizer配置短信供应商，请执行以下步骤：

1. 在左边栏中，浏览至 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL API凭据]** 菜单。 单击 **[!UICONTROL 创建新的API凭据]** 按钮。

   ![](assets/sms_6.png)

1. 配置SMS API凭据：

   * 对象 **[!DNL Sinch]**：

      * **[!UICONTROL 名称]**：选择API凭据的名称。

      * **[!UICONTROL 服务ID]** 和 **[!UICONTROL api令牌]**：访问API页面，您可以在SMS选项卡下找到凭据。  [了解详情](https://developers.sinch.com/docs/sms/getting-started/)
   * 对象 **[!DNL Twilio]**：

      * **[!UICONTROL 名称]**：选择API凭据的名称。

      * **[!UICONTROL 帐户SID]** 和 **[!UICONTROL 身份验证令牌]**：访问Twilio控制台仪表板页面的“帐户信息”窗格以查找凭据。

      * **[!UICONTROL 消息SID]**：输入分配给Twilio API创建的每条消息的唯一标识符。 [了解详情](https://support.twilio.com/hc/en-us/articles/223134387-What-is-a-Message-SID-)
   * 对象 **[!DNL Infobip]**：

      * **[!UICONTROL 名称]**：选择API凭据的名称。

      * **[!UICONTROL API基本URL]** 和 **[!UICONTROL api令牌]**：访问Web界面主页或API密钥管理页面以查找凭据。 [了解详情](https://www.infobip.com/docs/api)

   ![](assets/sms_7.png)

1. 单击 **[!UICONTROL 提交]** 完成API凭据配置时。

创建和配置API凭据后，您现在需要为SMS消息创建渠道界面（即消息预设）。

## 创建短信表面 {#message-preset-sms}

>[!CONTEXTUALHELP]
>id="ajo_admin_surface_sms_type"
>title="定义短信类别"
>abstract="选择使用此表面的短信消息类型：营销性的推广短信消息，此时需要用户同意；或者事务性的非商业短信消息，例如密码重置。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/privacy/consent/opt-out.html#sms-opt-out-management" text="选择退出营销短信消息"

配置短信渠道后，您必须创建一个渠道平面才能从中发送短信消息 **[!DNL Journey Optimizer]**.

要创建渠道表面，请执行以下步骤：

1. 在左边栏中，浏览至 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 并选择 **[!UICONTROL 品牌化]** > **[!UICONTROL 渠道表面]**. 单击 **[!UICONTROL 创建渠道表面]** 按钮。

   ![](assets/preset-create.png)

1. 输入表面的名称和描述（可选），然后选择短信渠道。

   ![](assets/sms_preset.png)

   >[!NOTE]
   >
   > 名称必须以字母(A-Z)开头。 它只能包含字母数字字符。 您也可以使用下划线 `_`，点`.` 和连字符 `-` 个字符。

1. 定义 **短信设置**.

   ![](assets/preset-sms.png)

   * 选择 **[!UICONTROL 短信类型]** 将随表面一起发送的内容： **[!UICONTROL 事务性]** 或 **[!UICONTROL 营销]**.

      * 选择 **营销** 促销短信：这些消息需要用户同意。
      * 选择 **事务性** 用于非商业性消息，例如订单确认、密码重置通知或投放信息。

      >[!CAUTION]
      >
      >**事务性** 短信消息可以发送给取消订阅营销通信的用户档案。 这些消息只能在特定上下文中发送。

      创建短信消息时，您必须选择与为消息选择的类别匹配的有效渠道平面。

   * 选择 **[!UICONTROL 短信配置]** 以与曲面相关联。

      有关如何配置环境以发送短信消息的更多信息，请参阅 [本节](#create-api).

   * 输入 **[!UICONTROL 发件人号码]** 您&#x200B;希望用于通信。

   * 选择您的 **[!UICONTROL 短信执行字段]** 以选择 **[!UICONTROL 配置文件属性]** 与用户档案的电话号码相关联。


1. 如果要在短信消息中使用URL缩短功能，请从 **[!UICONTROL 子域]** 列表。

   >[!NOTE]
   >
   >要能够选择子域，请确保您之前已配置至少一个短信子域。 [了解如何操作](sms-subdomains.md)

1. 配置完所有参数后，单击 **[!UICONTROL 提交]** 以确认。 也可以将渠道曲面另存为拔模，并稍后恢复其配置。

   ![](assets/sms_preset_2.png)

1. 创建渠道表面后，它显示在列表中，其中包含 **[!UICONTROL 正在处理]** 状态。

   >[!NOTE]
   >
   >如果检查不成功，请在中进一步了解失败的可能原因 [本节](#monitor-channel-surfaces).

1. 检查成功后，渠道表面将获得 **[!UICONTROL 活动]** 状态。 它可用于投放消息。

   ![](assets/preset-active.png)

您现在可以使用Journey Optimizer发送短信消息。

**相关主题**

* [创建短信消息](create-sms.md)
* [在历程中添加消息](../building-journeys/journeys-message.md)
* [在营销策划中添加消息](../campaigns/create-campaign.md)

