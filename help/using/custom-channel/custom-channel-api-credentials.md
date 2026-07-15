---
title: 管理自定义渠道的API凭据
description: 了解如何在Adobe Journey Optimizer中管理自定义渠道的API凭据。
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="有限发布版" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 4%

---


# 管理API凭据 {#api-credentials}

使用非&#x200B;**None**&#x200B;身份验证类型创建自定义渠道时，激活该渠道时会自动生成初始API凭据集。

您可以从&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 渠道生成器]** > **[!UICONTROL API凭据]**&#x200B;查看、管理和编辑凭据。

![API凭据](assets/custom_channel_api_credentials.png){width="100%"}

为同一渠道拥有多个凭据让您可以将不同的身份验证值附加到不同的渠道配置 — 例如，对于不同的品牌或用例 — 而不会复制渠道定义。

要编辑现有凭据集，请单击清单列表中的项目。 所有字段均可编辑。

要为同一渠道创建其他凭据，请执行以下步骤。

1. 从&#x200B;**[!UICONTROL API凭据]**&#x200B;列表中，单击&#x200B;**[!UICONTROL 创建API凭据]**。

1. 提供名称和描述。

   ![创建API凭据](assets/custom_channel_create_api_credentials.png){width="100%"}

1. 选择要为其创建凭据的&#x200B;**[!UICONTROL 渠道]**。

   >[!NOTE]
   >
   >下拉列表中仅显示身份验证类型为&#x200B;**无**&#x200B;以外的已激活自定义渠道。

1. 从列表中选择&#x200B;**[!UICONTROL 身份验证类型]**。
1. 填写特定于身份验证的字段：
   * **[!UICONTROL API密钥]** — 提供密钥名称、值和位置（查询参数或标头）。
   * **[!UICONTROL 基本身份验证]** — 提供用户名和密码。
   * **[!UICONTROL OAuth 2.0]** — 为OAuth 2.0身份验证配置有效负载。
1. 单击&#x200B;**[!UICONTROL 保存]**。

## 后续步骤 {#next-steps}

* [委派子域](custom-channel-subdomains.md)（可选 — 链接跟踪必需）
* [创建渠道配置](custom-channel-configuration.md)
