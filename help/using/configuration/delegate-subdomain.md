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
source-git-commit: 7854de133ebcd3b29ca59b747aa89fae242f2ea5
workflow-type: tm+mt
source-wordcount: '1897'
ht-degree: 16%

---

# 委派子域 {#delegate-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname"
>title="子域委派"
>abstract="Journey Optimizer 让您可以将子域委派给 Adobe。您可以将子域完全委派给 Adobe，这是推荐的方法。</br>您还可以使用CNAME创建子域以指向特定于Adobe的记录，但此方法要求您自行维护和管理DNS记录。"
>additional-url="https://experienceleague.adobe.com/zh-hans/docs/journey-optimizer/using/configuration/delegate-subdomains/about-subdomain-delegation#subdomain-delegation-methods" text="子域配置方法"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomainname_header"
>title="子域委派"
>abstract="要开始发送电子邮件，您需要将子域委派给 Adobe。委派完成后，将为您配置 DNS 记录、收件箱、发件人、回复地址和退回地址。"

域名委派是一种方法，它允许域名（技术上称为DNS区域）的所有者将其细分（技术上称为DNS区域下的细分）委派给另一个实体。 基本上，作为客户，如果您处理“example.com”区域，您可以将子区域“marketing.example.com”委派给Adobe。 了解有关[子域委派](about-subdomain-delegation.md)的更多信息

默认情况下，[!DNL Journey Optimizer]允许您最多委派&#x200B;**10个子域**。 但是，根据您的许可合同，您最多可以委派 100 个子域。请联系您的 Adobe 联系人，以进一步了解您有权使用的子域数量。

您可以：

* 完全委派子域 — [了解如何操作](#set-up-subdomain)
* 使用CNAME创建子域以指向特定于Adobe的记录 — [了解如何操作](#set-up-subdomain)

建议使用&#x200B;**完全子域委派**&#x200B;方法。 在[本节](about-subdomain-delegation.md#subdomain-delegation-methods)中了解不同子域配置方法之间的差异。

>[!CAUTION]
>
>[!DNL Journey Optimizer]不支持并行提交子域。 如果尝试在子域处于&#x200B;**[!UICONTROL 正在处理]**&#x200B;状态时提交子域以进行委派，则会收到一条错误消息。

## 访问委派的子域 {#access-delegated-subdomains}

所有委派的子域都显示在&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 子域]**&#x200B;菜单中。 筛选器可帮助您优化列表（委派日期、用户或状态）。

<!--![](assets/subdomain-list.png)-->

**[!UICONTROL 状态]**&#x200B;列提供了有关子域委派过程的信息：

* **[!UICONTROL 草稿]**：子域委派已另存为草稿。 单击子域名以继续执行委派过程，
* **[!UICONTROL 正在处理]**：子域正在经历多次配置检查，然后才能使用，
* **[!UICONTROL 成功]**：子域已成功通过检查，可用于传递消息，
* **[!UICONTROL 失败]**：提交子域委派后，一个或多个检查失败。

要访问有关状态为&#x200B;**[!UICONTROL 成功]**&#x200B;的子域的详细信息，请从列表中打开它。

![](assets/subdomain-delegated.png)

您可以：

* 检索在委派过程中配置的子域名（只读），以及生成的URL（资源、镜像页面、跟踪URL），

* 将Google网站验证TXT记录添加到子域，以确保其经过验证(请参阅[将Google TXT记录添加到子域](google-txt.md))。

>[!CAUTION]
>
>子域配置对所有环境通用。 因此，对子域的任何修改也会影响生产沙箱。

## 在Journey Optimizer中设置子域 {#set-up-subdomain}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns"
>title="生成匹配的 DNS 记录"
>abstract="要将新的子域完全委派给 Adobe，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息，复制粘贴到您的域托管解决方案中，以生成匹配的 DNS 记录。要使用 CNAME 委派子域，您还需要复制粘贴 SSL CDN URL 验证记录。检查成功后，子域就可以用来投放消息了。"

要在[!DNL Journey Optimizer]中设置新子域，请执行以下步骤。

>[!NOTE]
>
>本节介绍如何使用完全委派或CNAME方法设置子域。 [此部分](#setup-custom-subdomain)中详细介绍了自定义委派方法。


1. 访问&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL 设置子域]**。

   <!--![](assets/subdomain-delegate.png)-->

   >[!CAUTION]
   >
   >子域配置是&#x200B;**所有环境通用的配置**。 因此，对子域的任何修改也会影响生产沙箱。

1. 从&#x200B;**[!UICONTROL 设置方法]**&#x200B;部分中，选择：

   * 已完全委派 — [了解详情](about-subdomain-delegation.md#full-subdomain-delegation)
   * CNAME设置 — [了解详情](about-subdomain-delegation.md#cname-subdomain-setup)

     在此[专用部分](#cname-subdomain-setup)中了解如何使用CNAME设置子域

   <!--![](assets/subdomain-method-full.png)-->

1. 指定要委派的子域的名称。

   ![](assets/subdomain-name.png)

   >[!CAUTION]
   >
   >不允许将无效子域委派给Adobe。 确保输入贵组织拥有的有效子域，如marketing.yourcompany.com。
   >
   >无法使用相同的发送域从[!DNL Adobe Journey Optimizer]和其他产品（如[!DNL Adobe Campaign]或[!DNL Adobe Marketo Engage]）发送消息。

   <!--Capital letters are not allowed in subdomains. TBC by PM-->

1. 在专用部分中设置&#x200B;**[!UICONTROL DMARC记录]**。 如果子域现有[DMARC记录](dmarc-record.md)，并且由[!DNL Journey Optimizer]提取，则可以使用相同的值或根据需要更改它们。 如果不添加任何值，将使用默认值。 [了解如何管理DMARC记录](dmarc-record.md#set-up-dmarc)

   ![](assets/dmarc-record-found.png)

1. 在&#x200B;**[!UICONTROL DNS记录]**&#x200B;部分中，将显示要放置在DNS服务器中的记录列表。 逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

1. 确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“我确认……”框。

   ![](assets/subdomain-submit.png)

1. 如果要设置包含&#x200B;**CNAME**&#x200B;的子域，请转到[此部分](#cname-subdomain-setup)。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以使Adobe执行所需的检查。 [了解详情](#submit-subdomain)

## 使用 CNAME 设置子域 {#cname-subdomain-setup}

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_dns_cname"
>title="生成匹配的 DNS 和验证记录"
>abstract="要使用 CNAME 委派子域，您需要将 Journey Optimizer 界面中显示的 Adobe 名称服务器信息和 SSL CDN URL 验证记录，复制粘贴到您的托管 Platform 中。检查成功后，子域就可以用来投放消息了。"

>[!CONTEXTUALHELP]
>id="ajo_admin_subdomain_cdn_cname"
>title="复制验证记录"
>abstract="Adobe 生成验证记录。您需要在托管 Platform 上创建对应的记录，用于 CDN URL 验证。"

设置子域时，您可以使用CNAME指向特定于Adobe的记录。 使用此设置，您和Adobe共同负责维护DNS。

>[!CAUTION]
>
>如果贵组织的策略限制完全子域委派方法，则建议使用CNAME方法。 此方法要求您自行维护和管理DNS记录。
>
>Adobe将无法协助更改、维护或管理通过CNAME方法配置的子域的DNS。

要使用CNAME设置子域，请执行以下步骤。

1. 执行[此部分](#set-up-subdomain)中描述的所有步骤。

1. 在提交子域设置之前，您还需要完成一个步骤 — 单击&#x200B;**[!UICONTROL 继续]**。 请等待，直到Adobe验证在您的托管解决方案上生成的记录没有错误。 此过程最多可能需要2分钟。

   >[!NOTE]
   >
   >在继续之前，请确保已正确创建了所有记录。

1. Adobe生成一个SSL CDN URL验证记录。 将此验证记录复制到您的托管平台。 如果您已在托管解决方案上正确创建此记录，请选中“I confirm...”框。

1. 单击&#x200B;**[!UICONTROL 提交]**&#x200B;以使Adobe执行所需的检查。 [了解详情](#submit-subdomain)

➡️ [在此视频中了解如何使用CNAME创建子域以指向特定于Adobe的记录](#video)

## 提交子域设置 {#submit-subdomain}

要完成子域委派，请执行以下步骤。

1. 单击&#x200B;**[!UICONTROL 提交]**。

   >[!NOTE]
   >
   >如果尝试提交自定义子域时出错，请参阅[此部分](#check-list)。


1. 您可以使用&#x200B;**[!UICONTROL 另存为草稿]**&#x200B;按钮创建记录并稍后提交子域配置。

   >[!NOTE]
   >
   >然后，您可以通过从子域列表中打开子域委派来恢复子域委派。

1. 子域显示在状态为&#x200B;**[!UICONTROL 正在处理]**&#x200B;的列表中。 有关子域状态的详细信息，请参阅[此部分](#access-delegated-subdomains)。

   <!--![](assets/subdomain-processing.png)-->

1. 在能够使用该子域发送消息之前，您必须等待Adobe执行所需的检查，最多可能需要3小时。 [了解详情](#subdomain-validation)。

   >[!NOTE]
   >
   >在继续之前，请确保已正确创建了所有记录。

### 子域验证 {#subdomain-validation}

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

1. **创建PTR记录**： ISP需要PTR记录（也称为反向DNS记录），以便它们不会将电子邮件标记为垃圾邮件。 Gmail还建议为每个IP设置PTR记录。 仅当您首次委派子域时，Adobe才会创建PTR记录，每个IP对应一个记录，所有IP都指向该子域。 例如，如果IP是&#x200B;*192.1.2.1*，子域是&#x200B;*email.example.com*，则PTR记录将为： *192.1.2.1PTR r1.email.example.com*。 您可以稍后更新PTR记录以指向新的委派域。 [了解有关 PTR 记录的更多信息](ptr-records.md)

检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它随时可用于投放消息。

如果您无法在托管解决方案上创建验证记录，则子域将标记为&#x200B;**[!UICONTROL 失败]**。

验证记录后，Adobe会自动为子域创建PTR记录。 [了解详情](ptr-records.md)

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

完成后，联系Adobe代表，告知您要取消委派的子域。

Adobe处理您的请求后，未委派域不再显示在子域清单页面上。

>[!CAUTION]
>
>取消委派子域后，将应用以下内容：
>
>* 您无法重新激活使用该子域的渠道配置。
>* 您不能通过用户界面再次委派相同的子域。 如果您希望这样做，请联系您的Adobe代表。

## 操作说明视频{#video}

了解如何使用 CNAME 创建子域以指向特定于 Adobe 的记录。

>[!VIDEO](https://video.tv.adobe.com/v/342228?quality=12&captions=chi_hans)
