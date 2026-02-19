---
solution: Journey Optimizer
product: journey optimizer
title: 将电子邮件子域从CNAME迁移到自定义委派
description: 了解如何将电子邮件或登陆页子域从CNAME委派迁移到Journey Optimizer中的自定义委派。
feature: Subdomains, Deliverability
topic: Administration
role: Admin
level: Intermediate
keywords: 子域、委派、迁移、CNAME、自定义委派
badge: label="限量发布版" type="Informative"
source-git-commit: 316553be4f04e4fc0ae11bc767f7e48f64fc5ccd
workflow-type: tm+mt
source-wordcount: '1035'
ht-degree: 5%

---

# 将电子邮件子域从CNAME迁移到自定义委派 {#migrate-cname-to-custom}

>[!AVAILABILITY]
>
>此功能为限量发布版。请联系 Adobe 代表获取访问权限。

如果您的子域当前设置为[CNAME](about-subdomain-delegation.md#cname-subdomain-setup)，则可以将其迁移到&#x200B;**[!UICONTROL 自定义委派]**&#x200B;方法以满足您公司的安全策略。 这将为您提供对[!DNL Journey Optimizer]中子域和证书的完全所有权和控制权。 [了解有关自定义子域的更多信息](delegate-custom-subdomain.md)

在此过程中，您需要：

* 从您的托管解决方案中[删除现有DNS记录](#delete-dns)
* [上载从证书颁发机构获得的SSL证书](#upload-ssl-certificate)
* 通过验证域所有权和报告电子邮件地址，完成[反馈循环步骤](#feedback-loop)
* [将Adobe生成的SSL CDN URL验证记录](#copy-ssl-cdn-url-record)复制到您的托管平台

要迁移子域，请执行以下步骤。

## 开始之前 {#before-you-begin}

在开始迁移过程之前，请查看下面的重要信息。

>[!IMPORTANT]
>
>您只能迁移使用[CNAME方法](delegate-subdomain.md#cname-subdomain-setup)设置的子域。

* 确保为贵组织启用了&#x200B;**自定义委派方法**(此功能当前处于“有限可用性” — 请联系您的Adobe代表以获取访问权限)。 [了解详情](delegate-custom-subdomain.md)
* 确保没有活动渠道配置使用此子域。 迁移过程将中断其功能。
* 请确保任何活动的营销活动或历程均未使用链接到该子域的渠道配置，因为这可能会造成投放中断。
* 请注意，一旦进入迁移流程，停机时间就会开始。 在此过程中，子域将移至&#x200B;**[!UICONTROL 草稿]**，并且在安装程序完成之前不可用。
* 因此，建议在开始迁移过程之前&#x200B;**执行预迁移步骤**，以便准备好SSL证书并减少停机时间。 [了解详情](#start-migration)

## 开始迁移 {#start-migration}

请按照以下步骤开始迁移给定的子域。

1. 转到&#x200B;**[!UICONTROL 管理]** > **[!UICONTROL 渠道]** > **[!UICONTROL 电子邮件设置]** > **[!UICONTROL 子域]**。

1. 选择使用CNAME设置的子域并打开它。

1. 您可以使用&#x200B;**[!UICONTROL 预迁移CSR生成]**&#x200B;部分生成CSR以将其发送到证书颁发机构，并在迁移过程开始时准备好SSL证书。 [了解如何操作](#send-csr-to-ca)

   >[!IMPORTANT]
   >
   >在此阶段，预迁移步骤是可选的，但强烈建议这样做。 在&#x200B;**开始迁移前**&#x200B;完成迁移可减少停机时间并帮助确保顺利过渡。

   ![](assets/subdomain-migrate-pre-migration-csr.png){width="70%"}

1. 在专用部分中选择&#x200B;**[!UICONTROL 立即迁移]**。

   <!--![](assets/subdomain-migrate-to-custom.png){width=90%}-->

1. 查看显示的[信息](#before-you-begin)。

   >[!WARNING]
   >
   >进入迁移流后，停机时间就会开始，因此请确保它不会影响活动的活动和历程。

1. 单击&#x200B;**[!UICONTROL 是]**。 子域将移动到&#x200B;**[!UICONTROL 草稿]**&#x200B;状态，并且在安装程序完成之前不可用。

## 生成CSR并将其发送到证书颁发机构 {#send-csr-to-ca}

要完成迁移，您需要由证书颁发机构(CA)颁发的SSL证书。 要接收此SSL证书，您必须首先生成证书签名请求(CSR)并将其发送给CA。

无论您是否已启动迁移过程，请按照以下步骤生成并发送新的CSR。

1. 单击&#x200B;**[!UICONTROL 重新生成CSR]**。

1. 填写显示并重新生成证书签名请求(CSR)的表单。

   ![](assets/subdomain-migrate-regenerate-csr.png){width="60%"}

   >[!NOTE]
   >
   >密钥长度只能是 2048 位或 4096 位。子域提交后无法更改。

1. 单击&#x200B;**[!UICONTROL 下载CSR]**&#x200B;并将表单保存到本地计算机。

1. 将其发送到证书颁发机构(CA)以获取SSL证书。 在将此CSR提交给CA进行签名之前，需要考虑以下几点：

   * 步骤3中所下载的CSR仅适用于data.subdomain.com。

   * 但是，证书应将data.subdomain.com和cdn.subdomain.com作为主体备用名称(SAN)条目包含在单个证书中。 例如，如果您委派example.adobe.com ，则data.subdomain.com对应于data.example.adobe.com ，而cdn.subdomain.com对应于cdn.example.adobe.com。

   * 数据(data.example.adobe.com)和CDN (cdn.example.adobe.com)子域都需要作为对等项添加到同一证书中。

   * 大多数CA都允许您在签名过程中添加其他SAN（如CDN子域）

      * 通过CA门户（如果可用，推荐），或
      * 在门户选项不可用时，向其支持团队手动请求。

   * 签名后，CA将颁发单个证书，证书涵盖Data Domain和CDN子域。

## 删除现有DNS记录 {#delete-dns}

开始迁移过程后，您需要从托管解决方案中删除现有DNS记录。 请按照以下步骤操作。

1. 此时将显示当前在DNS服务器中配置的记录列表。

1. 导航到您的域托管解决方案，并从您的DNS托管中删除现有的CNAME条目。

1. 确保已删除所有DNS记录。 完成后，选中“我确认我已从托管站点中删除了所需记录”框。

   ![](assets/subdomain-migrate-delete-dns.png){width="75%"}

## 上传SSL证书 {#upload-ssl-certificate}

在&#x200B;**[!UICONTROL SSL证书]**&#x200B;部分中，您需要将新的SSL证书上载到[!DNL Journey Optimizer]。

在此之前，请验证以下各项：

* 如果您已经在[迁移前步骤](#start-migration)中将CSR发送到证书颁发机构，请确保已收到SSL证书。

* 如果您尚未这样做，请按照步骤[生成、下载和发送CSR](#send-csr-to-ca)。

<!--
    * Click **[!UICONTROL Regenerate CSR]** and fill the form to generate the Certificate Signing Request.

    * Click **[!UICONTROL Download CSR]** to save the form to your local computer.

    * Send the CSR to the Certificate Authority to get your SSL certificate.-->

1. 在检索SSL证书后，单击&#x200B;**[!UICONTROL 上载证书]**。

   ![](assets/subdomain-migrate-ssl-certificate.png){width="75%"}

1. 使用完整的证书链将.pem格式的SSL证书上载到[!DNL Journey Optimizer]。 以下是.pem文件格式的示例：

   ```
   -----BEGIN CERTIFICATE-----
   MIIDXTCCAkWgAwIBAgIJALc3... (base64 encoded data)
   -----END CERTIFICATE-----
   ```

1. 选中“我确认已上传SSL证书”框。

## 完整反馈环 {#feedback-loop}

然后，完成反馈循环步骤以验证域所有权和报告电子邮件地址。

![](assets/subdomain-migrate-feedback-loop.png){width="75%"}

此过程与设置新自定义子域时的过程相同。 按照[设置自定义子域](delegate-custom-subdomain.md#feedback-loop-steps)页面上详述的步骤操作。

## 复制SSL CDN URL验证记录 {#copy-ssl-cdn-url-record}

要完成迁移过程，请将Adobe生成的SSL CDN URL验证记录复制到您的托管平台。 此过程与设置新自定义子域时的过程相同。 按照[设置自定义子域](delegate-custom-subdomain.md#copy-ssl-cdn-url-record)页面上详述的步骤操作。

提交后，您必须等待Adobe执行所需的检查，最长可能需要3小时。 [了解详情](delegate-subdomain.md#submit-subdomain)

一旦子域再次处于活动状态，就无需更改使用该子域的现有渠道配置，它们将继续像以前一样工作。

**另请参阅**

* [设置自定义子域](delegate-custom-subdomain.md)
* [子域委派方法](about-subdomain-delegation.md#subdomain-delegation-methods)
