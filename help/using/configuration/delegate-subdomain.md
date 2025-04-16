---
solution: Journey Optimizer
product: journey optimizer
title: 委派子域
description: 了解如何委派子域。
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Experienced
keywords: 子域、委派、域、DNS
exl-id: 8021f66e-7725-475b-8722-e6f8d74c9023
source-git-commit: 8e5a904f9310385f5a8186159dedde9942624268
workflow-type: tm+mt
source-wordcount: '2009'
ht-degree: 20%

---

# 委派子域 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="子域委派"
>abstract="Journey Optimizer 让您可以将子域委派给 Adobe。您可以将子域完全委派给 Adobe，这是推荐的方法。您也可以使用 CNAME 创建子域，将其指向特定于 Adobe 的记录，但这种方法需要您自行维护和管理 DNS 记录。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="子域配置方法"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="子域委派"
>abstract="要开始发送电子邮件，您需要将子域委派给 Adobe。委派完成后，将为您配置 DNS 记录、收件箱、发件人、回复地址和退回地址。"

## 电子邮件子域入门 {#gs-delegate-subdomain}

域名委派是一种方法，它允许域名（技术上称为DNS区域）的所有者将其细分（技术上称为DNS区域下的细分）委派给另一个实体。 基本上，作为客户，如果您处理“example.com”区域，您可以将子区域“marketing.example.com”委派给Adobe。 了解有关[子域委派](about-subdomain-delegation.md)的更多信息

默认情况下，[!DNL Journey Optimizer]允许您最多委派&#x200B;**10个子域**。 但是，根据您的许可合同，您最多可以委派 100 个子域。请联系您的 Adobe 联系人，以进一步了解您有权使用的子域数量。

您可以完全委托子域，或使用CNAME创建子域以指向Adobe特定的记录。

建议使用完全子域委派。 了解有关[子域配置方法](about-subdomain-delegation.md#subdomain-delegation-methods)之间差异的详细信息。

子域配置&#x200B;**对所有环境通用**。 因此，对子域的任何修改也会影响生产沙盒。

>[!CAUTION]
>
>[!DNL Journey Optimizer]不支持并行提交子域。 如果尝试在子域处于&#x200B;**[!UICONTROL 正在处理]**&#x200B;状态时提交子域以进行委派，则会收到一条错误消息。

## 将子域完全委派给Adobe {#full-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要将新的子域完全委派给 Adobe，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，复制粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。要使用 CNAME 委派子域，您还需要复制粘贴 SSL CDN URL 验证记录。检查成功后，子域就可以用来投放消息了。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/configuration/delegate-subdomains/delegate-subdomain#cname-subdomain-delegation" text="CNAME 子域委派"

[!DNL Journey Optimizer]允许您直接从产品界面将子域完全委派给Adobe。 这样，Adobe将能够控制并维护发送、渲染和跟踪电子邮件营销活动所需的DNS的各个方面，从而作为托管服务来发送消息。

您可以依靠Adobe来维护所需的DNS基础架构，以满足电子邮件营销发送域的行业标准可投放性要求，同时继续维护和控制内部电子邮件域的DNS。

要将新子域完全委派给Adobe，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 设置子域]**。

   ![](assets/subdomain-delegate.png)

1. 从&#x200B;**[!UICONTROL 设置方法]**&#x200B;部分中选择&#x200B;**[!UICONTROL 已完全委派]**。

   ![](assets/subdomain-method-full.png)

1. 指定要委派的子域的名称。

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“我确认……”框。

   ![](assets/subdomain-submit.png)

1. 设置DMARC记录。 如果子域现有DMARC记录，并且它由[!DNL Journey Optimizer]获取，则您可以使用相同的值或根据需要更改它们。 如果不添加任何值，将使用默认值。 [了解详情](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. 单击&#x200B;**[!UICONTROL 提交]**。

   您可以使用&#x200B;**[!UICONTROL 另存为草稿]**&#x200B;按钮创建记录并稍后提交子域配置。 然后，您可以通过从子域列表中打开子域委派来恢复子域委派。

1. 子域显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的更多信息，请参阅[此部分](about-subdomain-delegation.md#access-delegated-subdomains)。

   ![](assets/subdomain-processing.png)

   在能够使用该子域发送消息之前，您必须等待Adobe执行所需的检查，这最多可能需要3个小时。 有关详细信息，请参阅[此部分](#subdomain-validation)。

   >[!NOTE]
   >
   >任何缺少的记录（即尚未在您的托管解决方案上创建的记录）都将被列出。

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL 成功]**&#x200B;状态。 它随时可用于投放消息。

   如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

在[!DNL Journey Optimizer]中将子域委派给Adobe后，将自动创建PTR记录并与该子域关联。 [了解详情](ptr-records.md)


## 使用CNAME设置子域 {#cname-subdomain-delegation}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="生成匹配的 DNS 和验证记录"
>abstract="要使用 CNAME 委派子域，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息和 SSL CDN URL 验证记录，复制粘贴到您的托管平台中。检查成功后，子域就可以用来投放消息了。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="复制验证记录"
>abstract="Adobe 生成验证记录。您需要在托管平台上创建对应的记录，用于 CDN URL 验证。"

如果您有特定于域的限制策略，并且希望Adobe仅对DNS具有部分控制权，则可以选择在您的一侧执行所有与DNS相关的活动。

CNAME子域设置允许您创建子域，并使用CNAME指向Adobe特定的记录。 使用此配置，您和 Adobe 共同负责维护 DNS，以设置用于发送、渲染和跟踪电子邮件的环境。

>[!CAUTION]
>
>如果贵组织的策略限制完全子域委派方法，则建议使用CNAME方法。 此方法要求您自行维护和管理DNS记录。 Adobe将无法帮助更改、维护或管理通过CNAME方法配置的子域的DNS。

➡️[了解如何在此视频中使用CNAME创建子域以指向Adobe特定的记录](#video)

要使用CNAME设置子域，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 通道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 设置子域]**。

1. 选择&#x200B;**[!UICONTROL CNAME设置]**&#x200B;方法。

   ![](assets/subdomain-method-cname.png)

1. 指定要委派的子域的名称。

   >[!CAUTION]
   >
   >不得将无效子域委派给Adobe。 请确保输入贵组织&#x200B;**拥有的**&#x200B;的有效子域，如marketing.yourcompany.com。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“我确认……”框。

   ![](assets/subdomain-create-dns-confirm.png)

1. 设置DMARC记录。 如果子域现有DMARC记录，并且它由[!DNL Journey Optimizer]获取，则您可以使用相同的值或根据需要更改它们。 如果不添加任何值，将使用默认值。 [了解详情](dmarc-record.md)

   ![](assets/dmarc-record-found.png)

1. 单击&#x200B;**[!UICONTROL 继续]**。

   稍后可以使用&#x200B;**[!UICONTROL 另存为草稿]**&#x200B;按钮创建记录。 然后，您可以在此阶段通过从子域列表中打开子域委托来恢复子域委派。

1. 等待至Adobe验证是否在您的托管解决方案上生成了无错误的记录。 此过程可能需要2分钟。

   >[!NOTE]
   >
   >任何缺少的记录（即尚未在您的托管解决方案上创建的记录）都将被列出。

1. Adobe生成一个SSL CDN URL验证记录。 将此验证记录复制到您的托管平台。 如果您已在托管解决方案上正确创建此记录，请选中“我确认……”框，然后单击&#x200B;**[!UICONTROL 提交]**。

   <!--![](assets/subdomain-cdn-url-validation.png)-->

1. 提交CNAME子域委派后，子域将显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](about-subdomain-delegation.md#access-delegated-subdomains)。

   ![](assets/subdomain-cname-processing.png)

   在能够使用该子域发送消息之前，您必须等待Adobe执行所需的检查，这通常需要2到3个小时。 有关详细信息，请参阅[此部分](#subdomain-validation)。

1. 一旦检查成功<!--i.e Adobe validates the record you created and installs it-->，子域将获得&#x200B;**[!UICONTROL 成功]**&#x200B;状态。 它随时可用于投放消息。

   如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

在验证记录并安装证书后，Adobe会自动为CNAME子域创建PTR记录。 [了解详情](ptr-records.md)


## 子域验证 {#subdomain-validation}

将执行以下检查和操作，直到验证子域并可用于发送消息为止。

这些步骤由Adobe执行，可能需要&#x200B;**最多3个小时**。

1. **预验证**：Adobe检查子域是否已委派给Adobe DNS（NS记录、SOA记录、区域设置、所有权记录）。 如果预验证步骤失败，则会返回一个错误及相应原因，否则Adobe会继续执行下一步。

1. **为域**&#x200B;配置DNS：

   * **MX记录**： Mail eXchange记录 — 处理发送到子域的入站电子邮件的邮件服务器记录。
   * **SPF记录**： Sender Policy Framework记录 — 列出可从子域发送电子邮件的邮件服务器的IP。
   * **DKIM记录**： DomainKeys Identified Mail标准记录 — 使用公钥 — 私钥加密对邮件进行身份验证以避免欺骗。
   * **A**：默认IP映射。
   * **CNAME**： Canonical Name或CNAME记录是将别名映射到true或canonical域名的DNS记录类型。

1. **创建跟踪和镜像URL**：如果域为email.example.com，则跟踪/镜像域将为data.email.example.com。 通过安装SSL证书对其进行保护。

1. **配置CDN CloudFront**：如果尚未设置CDN，则Adobe会为您组织的ID配置它。

1. **创建CDN域**：如果域为email.example.com，则CDN域将为cdn.email.example.com。

1. **创建并附加CDN SSL证书**： Adobe为CDN域创建CDN证书并将证书附加到CDN域。

1. **创建转发DNS**：如果这是您委派的第一个子域，Adobe将创建创建PTR记录所需的转发DNS — 每个IP各一个。

1. **创建PTR记录**： ISP需要PTR记录（也称为反向DNS记录），以便它们不会将电子邮件标记为垃圾邮件。 Gmail还建议为每个IP设置PTR记录。 仅当您首次委派子域时，Adobe才会创建PTR记录，每个IP对应一个记录，所有IP都指向该子域。 例如，如果IP是&#x200B;*192.1.2.1*，子域是&#x200B;*email.example.com*，则PTR记录将为： *192.1.2.1PTR r1.email.example.com*。 您可以稍后更新PTR记录以指向新的委派域。 [了解有关PTR记录的更多信息](ptr-records.md)

## 取消委派子域 {#undelegate-subdomain}

如果要取消委派子域，请联系您的Adobe代表。

但是，在与Adobe联系之前，您需要在用户界面中执行多个步骤。

>[!NOTE]
>
>您只能取消委派状态为&#x200B;**[!UICONTROL 成功]**&#x200B;的子域。 可以从用户界面中删除具有&#x200B;**[!UICONTROL 草稿]**&#x200B;和&#x200B;**[!UICONTROL 失败]**&#x200B;状态的子域。

首先，在[!DNL Journey Optimizer]中执行以下步骤：

1. 取消激活与子域关联的所有渠道配置。 [了解如何操作](../configuration/channel-surfaces.md#deactivate-a-surface)

1. 取消委派与此子域关联的任何登陆页面子域、短信子域和Web子域。

   您需要为每个[登陆页面](../landing-pages/lp-subdomains.md#undelegate-subdomain)、[短信](../sms/sms-subdomains.md#undelegate-subdomain)或[Web子域](../web/web-delegated-subdomains.md#undelegate-subdomain)提出专用请求。

1. 停止与子域关联的活动营销活动。 [了解如何操作](../campaigns/modify-stop-campaign.md#stop)

1. 停止与子域关联的活动历程。 [了解如何操作](../building-journeys/end-journey.md#stop-journey)

1. 将链接到子域的[PTR记录](ptr-records.md#edit-ptr-record)指向另一个子域。

   如果这是唯一委派的子域，则可以跳过此步骤。

完成后，请联系您的Adobe代表，询问您要取消委派的子域。

在Adobe处理您的请求后，未委派的域不再显示在子域清单页面上。

>[!CAUTION]
>
>取消委派子域之后：
>
>   * 您无法重新激活使用该子域的通道配置。
>   * 您不能通过用户界面再次委派确切的子域。 如果您希望这样做，请联系您的Adobe代表。

## 操作方法视频{#video}

了解如何使用 CNAME 创建子域以指向特定于 Adobe 的记录。

>[!VIDEO](https://video.tv.adobe.com/v/339484?quality=12)
