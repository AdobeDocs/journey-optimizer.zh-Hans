---
solution: Journey Optimizer
product: journey optimizer
title: 配置 Web 子域
description: 了解如何使用Journey Optimizer设置Web子域
role: Admin
level: Intermediate
keywords: Web，子域，配置
exl-id: 6503d9e6-6c6c-4a6d-ad3d-1d81eb3b4698
source-git-commit: 66ef57c263d29572ce0377e41bf0a8010e2f22d1
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 27%

---

# 配置 Web 子域 {#web-subdomains}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_header"
>title="委派 Web 子域"
>abstract="您将设置您的子域以供 Web 渠道使用。请从已委派给 Adobe 的子域中进行选择。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web"
>title="委派 Web 子域"
>abstract="如果您将来自 Adobe Experience Manager Assets Essentials 的内容添加到您的 Web 体验，则必须设置将用于发布此内容的子域。请从已委派给 Adobe 的子域中进行选择。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_web_default"
>title="设置 Web 子域"
>abstract="从委派给 Adobe 的子域的列表中选择一个子域。可将此 Web 子域设置为默认子域，但一次只能使用一个默认子域。"

在创作Web体验时，如果您添加来自 [Adobe Experience Manager Assets Essentials](../email/assets-essentials.md) 库中，您必须设置用于发布此内容的子域。

要执行此操作，您必须从已委派给Adobe的子域列表中进行选择。 了解有关将子域委派到的更多信息，请Adobe [此部分](../configuration/delegate-subdomain.md).

>[!CAUTION]
>
>Web子域配置对所有环境都是通用的。 因此：
>
>* 要访问和编辑Web子域，您必须具有 **[!UICONTROL 管理Web子域]** 对生产沙盒的权限。
>
> * 对Web子域的任何修改也会影响生产沙箱。


您可以创建多个Web子域，但 **默认** 子域。 您可以更改默认的Web子域，但一次只能使用一个子域。

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** 菜单，然后选择 **[!UICONTROL Web配置]** > **[!UICONTROL Web子域]**.

   ![](assets/web-access-subdomains.png)

1. 单击 **[!UICONTROL 设置子域]**.

1. 从列表中选择委派的子域。

   ![](assets/web-subdomain-details.png)

   >[!NOTE]
   >
   >无法选择已用作Web子域的子域。

1. 将自动添加在您的Web URL中显示的前缀。 你无法更改它。

1. 要将此子域设置为默认值，请选择相应的选项。

   ![](assets/web-subdomain-details-default.png)

   >[!NOTE]
   >
   >仅 **默认** 子域。

1. 单击&#x200B;**[!UICONTROL 提交]**. 子域获取 **[!UICONTROL 成功]** 状态。 它已准备好用于您的Web体验。

   >[!NOTE]
   >
   >在极少数情况下，子域设置可能会失败。 在这种情况下，您可以删除 **[!UICONTROL 失败]** 子域来使用 **[!UICONTROL 删除]** 按钮 **[!UICONTROL 更多操作]** 图标。

1. 的 **[!UICONTROL 默认]** 标记显示在当前用作默认的子域旁边。 要更改默认子域，请选择 **[!UICONTROL 设置为默认值]** 从 **[!UICONTROL 更多操作]** 按钮。

   >[!NOTE]
   >
   >您可以更改默认的Web子域，但一次只能使用一个子域。

   ![](assets/web-subdomain-default.png)

   <!--Only a subdomain with the **[!UICONTROL Success]** status can be set as default.

    You cannot delete a subdomain with the **[!UICONTROL Processing]** status.-->
