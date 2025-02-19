---
solution: Journey Optimizer
product: journey optimizer
title: 自定义操作疑难解答
description: 了解如何对自定义操作进行故障诊断
badge: label="有限发布版"
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 操作，第三方，自定义，历程， API
source-git-commit: d6501c8cc7e3293bd6a057d8e74654bced7dae75
workflow-type: tm+mt
source-wordcount: '582'
ht-degree: 2%

---


# 自定义操作疑难解答 {#troubleshoot-a-custom-action}

>[!AVAILABILITY]
>
>此功能仅适用于一组组织（限量发布）。 要获得访问权限，请与 Adobe 代表联系。
>

您可以通过从Journey Optimizer用户界面的“管理”部分发送API调用来测试自定义操作。 此功能可帮助您在历程中使用自定义操作之前或之后对其进行故障诊断。

作为管理员，使用&#x200B;**[!UICONTROL 发送测试请求]**&#x200B;功能，通过直接从Adobe Journey Optimizer发出真正的API调用来验证自定义操作配置。 此功能可确保请求结构、标头、身份验证和有效负载的格式正确，然后才能在历程中使用。

![](assets/send-test-request.png){width="70%" align="left"}

使用此功能可简化测试和验证过程，确保自定义操作在实时历程中正常运行。

## 先决条件 {#troubleshoot-custom-action-prereq}

要使用&#x200B;**[!UICONTROL 发送测试请求]**&#x200B;功能，必须使用URL、标头和身份验证设置预配置&#x200B;**自定义操作**。

管理员若要使用此功能，需要以下权限：

* 用户必须具有&#x200B;**[!DNL Manage journeys events, data sources and actions]**&#x200B;权限。
* 此权限包含在&#x200B;*历程管理员*&#x200B;角色中。
* 仅使用&#x200B;**[!DNL View journeys events]**&#x200B;权限是不够的。

在[本节](../administration/high-low-permissions.md#journey-capability)中了解有关历程权限的更多信息。

## 如何使用发送测试请求功能 {#troubleshoot-custom-action-use}

要测试自定义操作，请执行以下步骤：

1. 导航到&#x200B;**操作**&#x200B;配置屏幕，然后选择自定义操作。
1. 单击操作配置屏幕底部的&#x200B;**[!UICONTROL 发送测试请求]**按钮。
   在操作配置面板中![发送测试请求按钮](assets/test-request.png){width="70%" align="left"}
1. 在弹出窗口中，允许您指定请求参数：

   * 如果&#x200B;**自定义操作方法为GET**，则无需任何有效负载。
   * 如果&#x200B;**自定义操作方法为POST**，则必须提供JSON有效负载。

     >[!NOTE]
     >
     >如果此JSON的结构不正确，Adobe Journey Optimizer将引发错误；但是，如果数据类型不匹配，则不会引发此错误。 例如，如果将整数参数用于应该是字符串的内容，则不会发生错误。

   * 如果定义了身份验证，系统将提示您输入身份验证详细信息。

1. 单击&#x200B;**发送**&#x200B;以执行请求。
1. 来自API的响应（包括标头和状态代码）将显示在界面中。

## 身份验证处理 {#troubleshoot-custom-action-auth}

当自定义操作包括身份验证时，Adobe Journey Optimizer要求用户为每个测试请求输入身份验证详细信息：

* **基本身份验证：**&#x200B;用户必须提供&#x200B;*密码*。
* **API密钥身份验证：**&#x200B;用户必须输入API密钥&#x200B;*值*。
* **自定义身份验证：**&#x200B;用户必须在请求&#x200B;*bodyParam*&#x200B;中提供身份验证参数。 在此情况下添加了两个要完成的部分：**身份验证请求**&#x200B;和&#x200B;**身份验证响应**。

## 主要优点 {#troubleshoot-custom-action-benefits}

作为Journey Optimizer管理员，您还可以使用外部工具(例如Postman)来测试自定义操作。 与外部测试相比，产品内故障排除功能的主要优势如下：

* 测试请求由&#x200B;**AJO历程**&#x200B;执行，这意味着：

   * 使用确切的请求结构(包括Adobe Journey Optimizer特定的标头)。
   * 源IP和标头与实时历程中使用的相匹配。

* **[!UICONTROL 发送测试请求]**&#x200B;功能可用于对&#x200B;**实时历程**&#x200B;进行故障排除，因为已部署自定义操作。

* 这种产品内测试功能消除了手动在工具之间复制配置详细信息的需要，从而降低了错误风险。

## 故障排除 {#troubleshoot-custom-action-check}

如果请求失败，您可以检查：

* 在测试中输入的身份验证凭据。
* 请求方法(GET与POST)以及相应的有效负载。
* 在自定义操作中定义的API端点和标头。
* 使用响应数据识别潜在的错误配置。

