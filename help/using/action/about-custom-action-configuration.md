---
solution: Journey Optimizer
product: journey optimizer
title: 配置自定义操作
description: 了解如何配置自定义操作
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Experienced
keywords: 操作，第三方，自定义，历程， API
exl-id: 4df2fc7c-85cb-410a-a31f-1bc1ece237bb
source-git-commit: 12423d9fe07e5c757154ae4f732ff20ec6dc2427
workflow-type: tm+mt
source-wordcount: '1799'
ht-degree: 17%

---

# 配置自定义操作 {#configure-an-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_configuration"
>title="自定义操作"
>abstract="如果您要使用第三方系统发送消息，或者如果希望历程将 API 调用发送到第三方系统，请使用自定义操作配置第三方系统与历程的连接。例如，可以通过自定义操作连接到以下系统：Epsilon、Slack、[Adobe Developer](https://developer.adobe.com)、Firebase 等。"

如果您要使用第三方系统发送消息，或者如果希望历程将 API 调用发送到第三方系统，请使用自定义操作配置第三方系统与历程的连接。例如，您可以通过自定义操作连接到以下系统：Epsilon、Slack、 [Adobe Developer](https://developer.adobe.com){target="_blank"}、Firebase等。

自定义操作是由技术用户定义并提供给营销人员的附加操作。配置完毕后，它们会显示在历程的左侧面板的 **[!UICONTROL 操作]** 类别。 请参阅[此页面](../building-journeys/about-journey-activities.md#action-activities)以了解详情。

## 限制{#custom-actions-limitations}

自定义操作具有下列限制 [此页面](../start/guardrails.md).

在自定义操作参数中，您可以传递简单的集合以及对象集合。 在中了解有关收藏集限制的更多信息 [此页面](../building-journeys/collections.md#limitations).

另请注意，自定义操作参数具有预期格式（例如：字符串、小数等）。 必须注意遵守这些预期格式。 在本节中了解详情 [用例](../building-journeys/collections.md).

仅当使用时，自定义操作才支持JSON格式 [请求](../action/about-custom-action-configuration.md#define-the-message-parameters) 或 [响应负载](../action/action-response.md).

## 最佳实践{#custom-action-enhancements-best-practices}

在使用自定义操作选择要定位的端点时，请确保：

* 可以使用 [API 限制](../configuration/throttling.md) 或 [API 上限](../configuration/capping.md)的配置对此端点进行限制，从而支持历程的吞吐量。请注意，限制配置不能低于 200 TPS。任何目标端点都需要支持至少 200 TPS。
* 此端点的响应时间需要尽可能短。根据预期吞吐量，高响应时间可能会影响实际吞吐量。

为所有自定义操作定义了1分钟内300,000次调用的上限。 此外，默认上限按主机和沙盒执行。 例如，在沙盒上，如果您有两个具有相同主机的端点（例如：`https://www.adobe.com/endpoint1` 和 `https://www.adobe.com/endpoint2`），上限将适用于 adobe.com 主机下的所有端点。“endpoint1”和“endpoint2”将共享相同的上限配置，并且如果一个端点达到限制，将对另一个端点产生影响。

此限制是根据客户使用情况设置的，用于保护自定义操作所针对的外部端点。您需要在基于受众的历程中考虑这一点，相应地定义适当的读取率（使用自定义操作时为 5000 个用户档案/秒）。如果需要，您可以通过我们的“上限/限制 API”定义较大的上限或限制来覆盖此设置。请参阅[此页](../configuration/external-systems.md)。

出于以下各种原因，您不应使用自定义操作定位公共端点：

* 如果没有适当的上限或限制，则可能会向可能不支持此类卷的公共端点发送过多调用。
* 配置文件数据可以通过自定义操作发送，因此，定位公共端点可能会导致无意间在外部共享个人信息。
* 您对公共端点返回的数据没有控制权。 如果端点更改其API或开始发送错误信息，则这些信息将在发送的通信中可用，并可能产生负面影响。

## 同意和数据治理 {#privacy}

在Journey Optimizer中，您可以将数据治理和同意策略应用于自定义操作，以防止将特定字段导出到第三方系统，或排除未同意接收电子邮件、推送或短信通信的客户。 有关更多信息，请参阅以下页面：

* [数据治理](../action/action-privacy.md).
* [同意](../action/action-privacy.md).


## 配置步骤 {#configuration-steps}

以下是配置自定义操作所需的主要步骤：

1. 在“管理”菜单部分中，选择 **[!UICONTROL 配置]**. 在  **[!UICONTROL 操作]** 部分，单击 **[!UICONTROL 管理]**. 单击 **[!UICONTROL 创建操作]** 以创建新操作。 操作配置窗格将在屏幕右侧打开。

   ![](assets/custom2.png)

1. 输入操作的名称。

   >[!NOTE]
   >
   >只允许使用字母数字字符和下划线。 最大长度为30个字符。

1. 向操作添加描述。 此步骤是可选的。
1. 使用此操作的旅程数显示在 **[!UICONTROL 使用位置]** 字段。 您可以单击 **[!UICONTROL 查看历程]** 按钮以显示使用此操作的历程列表。
1. 定义不同的 **[!UICONTROL URL配置]** 参数。 请参阅[此页](../action/about-custom-action-configuration.md#url-configuration)。
1. 配置 **[!UICONTROL 身份验证]** 部分。 此配置与数据源的配置相同。  请参阅[此小节](../datasource/external-data-sources.md#custom-authentication-mode)。
1. 定义 **[!UICONTROL 操作参数]**. 请参阅[此页](../action/about-custom-action-configuration.md#define-the-message-parameters)。
1. 单击&#x200B;**[!UICONTROL 保存]**。

   自定义操作现已配置完毕，可随时用于您的历程。 请参阅[此页](../building-journeys/about-journey-activities.md#action-activities)。

   >[!NOTE]
   >
   >在历程中使用自定义操作时，大多数参数均为只读。 您只能修改 **[!UICONTROL 名称]**， **[!UICONTROL 描述]**， **[!UICONTROL URL]** 字段和 **[!UICONTROL 身份验证]** 部分。

## 端点配置 {#url-configuration}

配置自定义操作时，您需要定义以下内容 **[!UICONTROL 端点配置]** 参数：

![](assets/action-response1bis.png){width="70%" align="left"}

1. 在 **[!UICONTROL URL]** 字段，指定外部服务的URL：

   * 如果URL是静态的，请在此字段中输入URL。

   * 如果URL包含动态路径，则仅输入URL的静态部分，即方案、主机、端口，以及（可选）路径的静态部分。

     示例：`https://xxx.yyy.com/somethingstatic/`

     将自定义操作添加到历程时，您将指定URL的动态路径。 [了解详情](../building-journeys/using-custom-actions.md)。

   >[!NOTE]
   >
   >出于安全原因，我们强烈建议您对URL使用HTTPS方案。 我们不允许使用非公共Adobe地址和IP地址。
   >
   >定义自定义操作时只允许使用默认端口：80用于http，443用于https。

1. 选择呼叫 **[!UICONTROL 方法]**：它可以是以下任一类型 **[!UICONTROL POST]**， **[!UICONTROL GET]** 或 **[!UICONTROL PUT]**.

   >[!NOTE]
   >
   > 此 **DELETE** 方法不受支持。 如果需要更新现有资源，请选择 **PUT** 方法。

1. 定义标头和查询参数：

   * 在 **[!UICONTROL 标题]** 部分，单击 **[!UICONTROL 添加标题字段]** 定义发送到外部服务的请求消息的HTTP标头。 此 **[!UICONTROL Content-Type]** 和 **[!UICONTROL 字符集]** 默认设置标题字段。 您无法删除这些字段。 仅 **[!UICONTROL Content-Type]** 可以修改标头。 其值应遵循JSON格式。 以下是默认值：

   ![](assets/content-type-header.png)

   * 在 **[!UICONTROL 查询参数]** 部分，单击 **[!UICONTROL 添加查询参数字段]** 以定义要在URL中添加的参数。

   ![](assets/journeyurlconfiguration2bis.png)

1. 输入字段的标签或名称。

1. 选择类型： **[!UICONTROL 常量]** 或 **[!UICONTROL 变量]**. 如果您已选择 **[!UICONTROL 常量]**，然后在中输入常量值 **[!UICONTROL 值]** 字段。 如果您已选择 **[!UICONTROL 变量]**，则您将在向历程添加自定义操作时指定此变量。 [了解详情](../building-journeys/using-custom-actions.md)。

   ![](assets/journeyurlconfiguration2.png)

   >[!NOTE]
   >
   >将自定义操作添加到历程后，如果历程处于草稿状态，您仍然可以向历程添加标题或查询参数字段。 如果您不希望配置更改影响历程，请复制自定义操作并将字段添加到新的自定义操作。
   >
   >将根据字段解析规则验证标头。 了解详情，请参阅 [本文档](https://tools.ietf.org/html/rfc7230#section-3.2.4){_blank}.

## 定义有效负载参数 {#define-the-message-parameters}

1. 在 **[!UICONTROL 请求]** 部分中，粘贴要发送到外部服务的JSON有效负载示例。 此字段为可选字段，仅适用于POST和PUT调用方法。

1. 在 **[!UICONTROL 响应]** 部分中，粘贴由调用返回的有效负载示例。 此字段是可选字段，可用于所有调用方法。 有关如何在自定义操作中利用API调用响应的详细信息，请参阅 [此页面](../action/action-response.md).

>[!NOTE]
>
>响应功能目前在Beta版中可用。

![](assets/action-response2bis.png){width="70%" align="left"}

>[!NOTE]
>
>有效负载示例不能包含null值。 有效负载中的字段名称不能包含“。” 字符。不能以“$”字符开头。

您将能够定义参数类型（例如：字符串、整数等）。

您还可以在指定参数是常量还是变量之间进行选择：

* **常量** 表示参数的值由技术角色在操作配置窗格中定义。 值将在各个历程中始终相同。 此操作不会有所不同，并且营销人员在历程中使用自定义操作时不会看到它。 例如，它可能是第三方系统期望的ID。 在这种情况下，切换常量/变量右侧的字段是传递的值。
* **变量** 表示参数的值将发生变化。 在历程中使用此自定义操作的营销人员可以自由传递他们想要的值，或指定在何处检索此参数的值(例如，从事件、Adobe Experience Platform等)。 在这种情况下，切换常量/变量右侧的字段是营销人员将在历程中看到的用于命名此参数的标签。

![](assets/customactionpayloadmessage2.png)

## mTLS协议支持 {#mtls-protocol-support}

您现在可以使用相互传输层安全性(mTLS)来确保与HTTP API目标和Adobe Journey Optimizer自定义操作的出站连接中的增强安全性。 mTLS是一种用于相互身份验证的端到端安全方法，可确保共享信息的双方在数据共享之前都是声称的身份。 与TLS相比，mTLS还包括一个附加步骤，在该步骤中，服务器还会请求客户端的证书并在其末尾验证它。

在Adobe Journey Optimizer中，mTLS与自定义操作结合使用。 您无需为Adobe Journey Optimizer自定义操作进行其他配置即可启用mTLS。 当自定义操作的端点启用了mTLS时，系统会从Adobe Experience Platform密钥库获取证书并自动将其提供给端点（这是mTLS连接所必需的）。

如果要将mTLS与这些Adobe Journey Optimizer和Experience PlatformHTTP API目标工作流结合使用，则置入Adobe Journey Optimizer客户操作UI或目标UI的服务器地址必须禁用TLS协议，并且仅启用mTLS。 如果该端点上仍启用TLS 1.2协议，则不会为客户端身份验证发送证书。 这意味着要将mTLS与这些工作流结合使用，您的“接收”服务器端点必须是mTLS **仅限** 已启用连接端点。

>[!IMPORTANT]
>
>在激活mTLS的Adobe Journey Optimizer自定义操作或历程中不需要任何其他配置；当检测到启用了mTLS的端点时，此过程会自动发生。 每个证书的通用名称(CN)和使用者可选名称(SAN)都作为证书的一部分在文档中提供，并且您可以根据需要用作所有权验证的附加层。
>
>2000年5月发布的RFC 2818不再使用HTTPS证书中的公用名(CN)字段进行使用者名称验证。 它建议改用“dns名称”类型的“使用者可选名称”扩展(SAN)。

如果要检查CN或SAN进行其他第三方验证，可以在此处下载相关证书：

```
Prod:
{
    "serviceName": "AJO Journeys",
    "publicCertificate": "-----BEGIN CERTIFICATE-----
MIIG9TCCBd2gAwIBAgIQBX+pDP5hB0gqDzFKyq5wLjANBgkqhkiG9w0BAQsFADBZ
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMTMwMQYDVQQDEypE
aWdpQ2VydCBHbG9iYWwgRzIgVExTIFJTQSBTSEEyNTYgMjAyMCBDQTEwHhcNMjQw
NTA5MDAwMDAwWhcNMjUwNjA5MjM1OTU5WjB0MQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTERMA8GA1UEBxMIU2FuIEpvc2UxEzARBgNVBAoTCkFkb2Jl
IEluYy4xKDAmBgNVBAMTH2Fqby1qb3VybmV5cy5hZXAtbXRscy5hZG9iZS5jb20w
ggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQDaI8HZHzbmPEgTy9O7cYmq
ZVX5283Gw7j7v4/O810jZXItBDmsSiWotvTgAT0s2oZMZZ6tGPbQB7hL+xJJ+yu2
HxFl1WzB4UGHJ+UbrL94hI930xQs0FVgSOGgIarj5HucF2ZxwHIkVHY5whrOq9t4
UxFBG0siUPQrTzV9GfA0wREElugpTbwaM8CTWwOQ9ekroOD2C5zAcLTycXFtSMiU
B4L4u38S9hGoBByzzKv9GnUMQudvt/s5zsGykZgEEYeN6IitfVO6BOD9jT94Aytx
/O3XH5w8v4KNTn+An99bXFmyg3JRUFSYZFxha8s1f6uu0XbdToQ+ao0WkE06nMmV
AgMBAAGjggOcMIIDmDAfBgNVHSMEGDAWgBR0hYDAZsffN97PvSk3qgMdvu3NFzAd
BgNVHQ4EFgQUn8OqtzccNdrsb+fbRnTHmtTZxLMwKgYDVR0RBCMwIYIfYWpvLWpv
dXJuZXlzLmFlcC1tdGxzLmFkb2JlLmNvbTA+BgNVHSAENzA1MDMGBmeBDAECAjAp
MCcGCCsGAQUFBwIBFhtodHRwOi8vd3d3LmRpZ2ljZXJ0LmNvbS9DUFMwDgYDVR0P
AQH/BAQDAgWgMB0GA1UdJQQWMBQGCCsGAQUFBwMBBggrBgEFBQcDAjCBnwYDVR0f
BIGXMIGUMEigRqBEhkJodHRwOi8vY3JsMy5kaWdpY2VydC5jb20vRGlnaUNlcnRH
bG9iYWxHMlRMU1JTQVNIQTI1NjIwMjBDQTEtMS5jcmwwSKBGoESGQmh0dHA6Ly9j
cmw0LmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAy
MENBMS0xLmNybDCBhwYIKwYBBQUHAQEEezB5MCQGCCsGAQUFBzABhhhodHRwOi8v
b2NzcC5kaWdpY2VydC5jb20wUQYIKwYBBQUHMAKGRWh0dHA6Ly9jYWNlcnRzLmRp
Z2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbEcyVExTUlNBU0hBMjU2MjAyMENBMS0x
LmNydDAMBgNVHRMBAf8EAjAAMIIBfwYKKwYBBAHWeQIEAgSCAW8EggFrAWkAdwBO
daMnXJoQwzhbbNTfP1LrHfDgjhuNacCx+mSxYpo53wAAAY9ecsWsAAAEAwBIMEYC
IQDQclgq89ZVlwdYBJFEIs8q4WIcZ9Siw+jb9OgCrz+wjwIhALQLnC1WyT+dHjvY
FvZjc99WkjnEwhIevj/Rz7r0EzhmAHUAfVkeEuF4KnscYWd8Xv340IdcFKBOlZ65
Ay/ZDowuebgAAAGPXnLF5AAABAMARjBEAiBy9cNT3CnmSMOdJe+JbG8f7ha1UGgN
TdDlaR9x9fKmKQIgNmGjz5AzP1evB2G1TTvVLkHfWQw0864c4F23WSV+6TsAdwDP
EVbu1S58r/OHW9lpLpvpGnFnSrAX7KwB0lt3zsw7CAAAAY9ecsYnAAAEAwBIMEYC
IQCTcB7s1xDP8Olif3jj4X8jHgVxv5C3bTvG6wDYBByfcQIhAOt8PhR6tWSLtF1V
HB8r7dns7Oth1+QT7WMonQZsP/3WMA0GCSqGSIb3DQEBCwUAA4IBAQAjTy45fbQV
aVTZ71wcIyHnkJfq/8SSc/UNT5//6AMiV6kb3YsFW1+EaQ1wPHZS0Qfjs7aIsXi5
f2TCGps8onELNpOfFfptrOCMfcYGMvV1wPCBy+kuoGY/YRZlsdNUTTzQAGztfRev
79w+XIDzioCrY+sfyUkkw+N/F7/RIjzMKjP6onSfuD+5WjqVKq9kFE0fCyJixedV
BPoPM4Cktgvc9SsK17JmLWkg+V2yH1eDzmjF3sR0/dcmoAM0qgV/CDuhIIqX2o7m
3/aQSNsPUpgBVbkz+SjEtchmw8DXW/Kro8QVulsXdbkiLTOj4JopxdOzrbKgWMwr
pIw7KKJoktDk
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIEyDCCA7CgAwIBAgIQDPW9BitWAvR6uFAsI8zwZjANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0yMTAzMzAwMDAwMDBaFw0zMTAzMjkyMzU5NTlaMFkxCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxMzAxBgNVBAMTKkRpZ2lDZXJ0IEdsb2Jh
bCBHMiBUTFMgUlNBIFNIQTI1NiAyMDIwIENBMTCCASIwDQYJKoZIhvcNAQEBBQAD
ggEPADCCAQoCggEBAMz3EGJPprtjb+2QUlbFbSd7ehJWivH0+dbn4Y+9lavyYEEV
cNsSAPonCrVXOFt9slGTcZUOakGUWzUb+nv6u8W+JDD+Vu/E832X4xT1FE3LpxDy
FuqrIvAxIhFhaZAmunjZlx/jfWardUSVc8is/+9dCopZQ+GssjoP80j812s3wWPc
3kbW20X+fSP9kOhRBx5Ro1/tSUZUfyyIxfQTnJcVPAPooTncaQwywa8WV0yUR0J8
osicfebUTVSvQpmowQTCd5zWSOTOEeAqgJnwQ3DPP3Zr0UxJqyRewg2C/Uaoq2yT
zGJSQnWS+Jr6Xl6ysGHlHx+5fwmY6D36g39HaaECAwEAAaOCAYIwggF+MBIGA1Ud
EwEB/wQIMAYBAf8CAQAwHQYDVR0OBBYEFHSFgMBmx9833s+9KTeqAx2+7c0XMB8G
A1UdIwQYMBaAFE4iVCAYlebjbuYP+vq5Eu0GF485MA4GA1UdDwEB/wQEAwIBhjAd
BgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwdgYIKwYBBQUHAQEEajBoMCQG
CCsGAQUFBzABhhhodHRwOi8vb2NzcC5kaWdpY2VydC5jb20wQAYIKwYBBQUHMAKG
NGh0dHA6Ly9jYWNlcnRzLmRpZ2ljZXJ0LmNvbS9EaWdpQ2VydEdsb2JhbFJvb3RH
Mi5jcnQwQgYDVR0fBDswOTA3oDWgM4YxaHR0cDovL2NybDMuZGlnaWNlcnQuY29t
L0RpZ2lDZXJ0R2xvYmFsUm9vdEcyLmNybDA9BgNVHSAENjA0MAsGCWCGSAGG/WwC
ATAHBgVngQwBATAIBgZngQwBAgEwCAYGZ4EMAQICMAgGBmeBDAECAzANBgkqhkiG
9w0BAQsFAAOCAQEAkPFwyyiXaZd8dP3A+iZ7U6utzWX9upwGnIrXWkOH7U1MVl+t
wcW1BSAuWdH/SvWgKtiwla3JLko716f2b4gp/DA/JIS7w7d7kwcsr4drdjPtAFVS
slme5LnQ89/nD/7d+MS5EHKBCQRfz5eeLjJ1js+aWNJXMX43AYGyZm0pGrFmCW3R
bpD0ufovARTFXFZkAdl9h6g4U5+LXUZtXMYnhIHUfoyMo5tS58aI7Dd8KvvwVVo4
chDYABPPTHPbqjc1qCmBaZx2vN4Ye5DUys/vZwP9BFohFrH/6j/f3IL16/RZkiMN
JCqVJUzKoZHm1Lesh3Sz8W2jmdv51b2EQJ8HmA==
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
MIIDjjCCAnagAwIBAgIQAzrx5qcRqaC7KGSxHQn65TANBgkqhkiG9w0BAQsFADBh
MQswCQYDVQQGEwJVUzEVMBMGA1UEChMMRGlnaUNlcnQgSW5jMRkwFwYDVQQLExB3
d3cuZGlnaWNlcnQuY29tMSAwHgYDVQQDExdEaWdpQ2VydCBHbG9iYWwgUm9vdCBH
MjAeFw0xMzA4MDExMjAwMDBaFw0zODAxMTUxMjAwMDBaMGExCzAJBgNVBAYTAlVT
MRUwEwYDVQQKEwxEaWdpQ2VydCBJbmMxGTAXBgNVBAsTEHd3dy5kaWdpY2VydC5j
b20xIDAeBgNVBAMTF0RpZ2lDZXJ0IEdsb2JhbCBSb290IEcyMIIBIjANBgkqhkiG
9w0BAQEFAAOCAQ8AMIIBCgKCAQEAuzfNNNx7a8myaJCtSnX/RrohCgiN9RlUyfuI
2/Ou8jqJkTx65qsGGmvPrC3oXgkkRLpimn7Wo6h+4FR1IAWsULecYxpsMNzaHxmx
1x7e/dfgy5SDN67sH0NO3Xss0r0upS/kqbitOtSZpLYl6ZtrAGCSYP9PIUkY92eQ
q2EGnI/yuum06ZIya7XzV+hdG82MHauVBJVJ8zUtluNJbd134/tJS7SsVQepj5Wz
tCO7TG1F8PapspUwtP1MVYwnSlcUfIKdzXOS0xZKBgyMUNGPHgm+F6HmIcr9g+UQ
vIOlCsRnKPZzFBQ9RnbDhxSJITRNrw9FDKZJobq7nMWxM4MphQIDAQABo0IwQDAP
BgNVHRMBAf8EBTADAQH/MA4GA1UdDwEB/wQEAwIBhjAdBgNVHQ4EFgQUTiJUIBiV
5uNu5g/6+rkS7QYXjzkwDQYJKoZIhvcNAQELBQADggEBAGBnKJRvDkhj6zHd6mcY
1Yl9PMWLSn/pvtsrF9+wX3N3KjITOYFnQoQj8kVnNeyIv/iPsGEMNKSuIEyExtv4
NeF22d+mQrvHRAiGfzZ0JFrabA0UWTW98kndth/Jsw1HKj2ZL7tcu7XUIOGZX1NG
Fdtom/DzMNU+MeKNhJ7jitralj41E6Vf8PlwUHBHQRFXGU7Aj64GxJUTFy8bJZ91
8rGOmaFvE7FBcf6IKshPECBV1/MUReXgRPTqh5Uykw7+U0b6LJ3/iyK5S9kJRaTe
pLiaWN0bfVKfjllDiIGknibVb63dDcY3fe0Dkhvld1927jyNxF1WW6LZZm6zNTfl
MrY=
-----END CERTIFICATE-----",
    "expiryDate": "2025-06-09T23:59:59Z"
}
```

