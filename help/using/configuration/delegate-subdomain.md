---
solution: Journey Optimizer
product: journey optimizer
title: 委派子域
description: 了解如何委派子域。
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: 子域、委派、域、DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 54ea3573e4fb6e24c3e56349292528bc6da42d67
workflow-type: tm+mt
source-wordcount: '1757'
ht-degree: 23%

---

# 委派子域 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="子域委派"
>abstract="Journey Optimizer 让您可以将子域委派给 Adobe。您可以将子域完全委派给 Adobe，这是推荐的方法。您也可以使用 CNAME 创建子域，将其指向特定于 Adobe 的记录，但这种方法需要您自行维护和管理 DNS 记录。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation.html?lang=zh-Hans#subdomain-delegation-methods" text="子域配置方法"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="子域委派"
>abstract="要开始发送电子邮件，您需要将子域委派给 Adobe。委派完成后，将为您配置 DNS 记录、收件箱、发件人、回复地址和退回地址。"

域名委派是一种方法，允许域名（技术上称为DNS区域）的所有者将其细分（技术上称为DNS区域，可称为子区域）委派给其他实体。 基本上，作为客户，如果您处理“example.com”区域，您可以将子区域“marketing.example.com”委派给Adobe。 详细了解 [子域委派](about-subdomain-delegation.md)

>[!NOTE]
>
>默认情况下， [!DNL Journey Optimizer] 许可合同允许您最多委派10个子域。 如果您希望增加此限制，请联系您的Adobe联系人。

您可以完全委派子域，也可以使用CNAME创建子域以指向特定于Adobe的记录。

>[!CAUTION]
>
>建议使用完全子域委派方法。 了解关于两者之间差异的更多信息 [子域配置方法](about-subdomain-delegation.md#subdomain-delegation-methods).
>
>子域配置对所有环境通用。 因此，对子域的任何修改也会影响生产沙箱。

## 完全子域委派 {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要将新的子域完全委派给 Adobe，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，复制粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。要使用 CNAME 委派子域，您还需要复制粘贴 SSL CDN URL 验证记录。检查成功后，子域就可以用来传递消息了。"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain.html?lang=zh-Hans#cname-subdomain-delegation" text="CNAME 子域委派"

[!DNL Journey Optimizer] 允许您将子域完全委派给直接从产品界面Adobe。 这样，Adobe将能够控制并维护发送、渲染和跟踪电子邮件营销活动所需的DNS的各个方面，从而作为托管服务来发送消息。

您可以依靠Adobe来维护所需的DNS基础架构，以满足电子邮件营销发送域的行业标准可投放性要求，同时继续维护和控制内部电子邮件域的DNS。

要将新子域完全委派给Adobe，请执行以下步骤：

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 子域]** 菜单，然后单击 **[!UICONTROL 设置子域]**.

   ![](assets/subdomain-delegate.png)

1. 选择 **[!UICONTROL 已完全委派]** 从 **[!UICONTROL 设置方法]** 部分。

   ![](assets/subdomain-method-full.png)

1. 指定要委派的子域的名称。

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“I confirm...”框，然后单击 **[!UICONTROL 提交]**.

   ![](assets/subdomain-submit.png)

   >[!NOTE]
   >
   >您可以创建记录，并稍后使用提交子域配置。 **[!UICONTROL 另存为草稿]** 按钮。 然后，您可以通过从子域列表中打开子域委派来恢复子域委派。

1. 提交完全子域委派后，子域将显示在列表中，其中包含 **[!UICONTROL 正在处理]** 状态。 有关子域状态的更多信息，请参阅 [本节](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-processing.png)

   在能够使用该子域发送消息之前，您必须等待Adobe执行所需的检查，这最多可能需要3小时。 有关详细信息，请参阅[此部分](#subdomain-validation)。

   >[!NOTE]
   >
   >任何丢失的记录（即尚未在您的托管解决方案上创建的记录）都将列出。

1. 检查成功后，子域将获得 **[!UICONTROL 成功]** 状态。 它可用于投放消息。

   >[!NOTE]
   >
   >该子域将标记为 **[!UICONTROL 失败]** 如果您无法在托管解决方案上创建验证记录。

将子域委派给Adobe后，在 [!DNL Journey Optimizer]，则会自动创建一个PTR记录并与此子域关联。 [了解详情](ptr-records.md)

>[!CAUTION]
>
>当前不支持并行执行子域 [!DNL Journey Optimizer]. 如果您尝试提交子域进行委派，而另一个子域具有 **[!UICONTROL 正在处理]** 状态，您会收到一条错误消息。

## CNAME 子域委派 {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="生成匹配的 DNS 和验证记录"
>abstract="要使用 CNAME 委派子域，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息和 SSL CDN URL 验证记录，复制粘贴到您的托管平台中。检查成功后，子域就可以用来传递消息了。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="复制验证记录"
>abstract="Adobe 生成验证记录。您需要在托管平台上创建对应的记录，用于 CDN URL 验证。"

如果您有特定于域的限制策略，并且希望Adobe仅对DNS具有部分控制权，则可以选择在您的一侧执行所有与DNS相关的活动。

CNAME 子域委派允许您创建子域，并使用 CNAME 指向特定于 Adobe 的记录。使用此配置，您和 Adobe 共同负责维护 DNS，以设置用于发送、渲染和跟踪电子邮件的环境。

>[!CAUTION]
>
>如果贵组织的策略限制完全子域委派方法，则建议使用CNAME方法。 此方法要求您自行维护和管理DNS记录。 Adobe将无法帮助更改、维护或管理通过CNAME方法配置的子域的DNS。

➡️ [在此视频中了解如何使用CNAME创建子域以指向特定于Adobe的记录](#video)

要使用CNAME委派子域，请执行以下步骤：

1. 访问 **[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 子域]** 菜单，然后单击 **[!UICONTROL 设置子域]**.

1. 选择 **[!UICONTROL CNAME设置]** 方法。

   ![](assets/subdomain-method-cname.png)

1. 指定要委派的子域的名称。

   >[!CAUTION]
   >
   >不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“I confirm...”框。

   ![](assets/subdomain-create-dns-confirm.png)

   >[!NOTE]
   >
   >稍后可以使用创建记录 **[!UICONTROL 另存为草稿]** 按钮。 此时，您可以通过从子域列表中打开子域委派来恢复子域委派。

1. 请等待，直到Adobe验证在您的托管解决方案上生成这些记录时没有出现错误。 此过程最多可能需要2分钟。

   >[!NOTE]
   >
   >任何丢失的记录（即尚未在您的托管解决方案上创建的记录）都将列出。

1. Adobe生成SSL CDN URL验证记录。 将此验证记录复制到您的托管平台。 如果您已在托管解决方案上正确创建此记录，请选中“I confirm...”框，然后单击 **[!UICONTROL 提交]**.

   <!--![](assets/subdomain-cdn-url-validation.png)-->

   >[!NOTE]
   >
   >您还可以创建验证记录，并稍后使用提交子域配置。 **[!UICONTROL 另存为草稿]** 按钮。 然后，您可以通过从子域列表中打开子域委派来恢复子域委派。

1. 提交CNAME子域委派后，子域显示在列表中，其中包含 **[!UICONTROL 正在处理]** 状态。 有关子域状态的更多信息，请参阅 [本节](about-subdomain-delegation.md#access-delegated-subdomains).

   ![](assets/subdomain-cname-processing.png)

   在能够使用该子域发送消息之前，您必须等待Adobe执行所需的检查，这通常需要2到3小时。 有关详细信息，请参阅[此部分](#subdomain-validation)。

1. 检查成功后<!--i.e Adobe validates the record you created and installs it-->，子域将获得 **[!UICONTROL 成功]** 状态。 它可用于投放消息。

   >[!NOTE]
   >
   >该子域将标记为 **[!UICONTROL 失败]** 如果您无法在托管解决方案上创建验证记录。

在验证记录并安装证书后，Adobe会自动为CNAME子域创建PTR记录。 [了解详情](ptr-records.md)

>[!CAUTION]
>
>当前不支持并行执行子域 [!DNL Journey Optimizer]. 如果您尝试提交子域进行委派，而另一个子域具有 **[!UICONTROL 正在处理]** 状态，您会收到一条错误消息。

## 子域验证 {#subdomain-validation}

将执行以下检查和操作，直到验证子域并可用于发送消息为止。

>[!NOTE]
>
>这些步骤由Adobe执行，最长可能需要3小时。

1. **预验证**：Adobe检查子域是否已委派给AdobeDNS（NS记录、SOA记录、区域设置、所有权记录）。 如果预验证步骤失败，则会返回一个错误及相应原因，否则Adobe会继续执行下一步。

1. **为域配置DNS**：

   * **MX记录**：邮件交换记录 — 处理发送到子域的入站电子邮件的邮件服务器记录。
   * **SPF记录**：发件人策略框架记录 — 列出可从子域发送电子邮件的邮件服务器的IP。
   * **DKIM记录**：DomainKeys Identified Mail标准记录 — 使用公钥 — 私钥加密对消息进行身份验证以避免欺骗。
   * **A**：默认IP映射。
   * **CNAME**：规范名称或CNAME记录是一种将别名映射到真实或规范域名的DNS记录类型。

1. **创建跟踪和镜像URL**：如果域是email.example.com，则跟踪/镜像域将为data.email.example.com。 通过安装SSL证书对其进行保护。

1. **配置CDN CloudFront**：如果尚未设置CDN，则Adobe会为贵组织的ID设置它。

1. **创建CDN域**：如果域是email.example.com，则CDN域将为cdn.email.example.com。

1. **创建和附加CDN SSL证书**：Adobe为CDN域创建CDN证书，并将该证书附加到CDN域。

1. **创建转发DNS**：如果这是您委派的第一个子域，则Adobe将创建转发DNS，这是创建PTR记录所必需的 — 每个IP各一个DNS。

1. **创建PTR记录**：ISP需要使用PTR记录（也称为反向DNS记录），以免他们将电子邮件标记为垃圾邮件。 Gmail还建议每个IP都有PTR记录。 仅当您首次委派子域时，Adobe才会创建PTR记录，每个IP创建一个记录，所有IP都指向该子域。 例如，如果IP *192.1.2.1* 子域为 *email.example.com*，则PTR记录将为： *192.1.2.1 PTR r1.email.example.com*. 之后，您可以更新PTR记录以指向新的委派域。 [了解有关PTR记录的更多信息](ptr-records.md)

## 操作方法视频{#video}

了解如何使用 CNAME 创建子域以指向特定于 Adobe 的记录。

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
