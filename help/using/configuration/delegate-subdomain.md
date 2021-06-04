---
title: 委派子域
description: 了解如何委派子域
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
source-git-commit: e569e992530df5429ffb96f78ba28b53de0ded81
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 8%

---


# 委派子域

域名委派是允许域名所有者的方法(技术上为：DNS区域)，以委派其分区(技术上：其下的DNS区域（可称为子区域）到其他实体。 基本上，如果客户正在处理区域“example.com”，他可以将子区域“marketing.example.com”委派给Adobe。

通过委派子域以与Adobe Optimizer一起使用，客户可以依赖Adobe来维护满足其电子邮件营销发送域行业标准可交付性要求所需的DNS基础结构，同时继续维护和控制其的DNS
内部电子邮件域。

Journey Optimizer允许您将子域完全委派给Adobe。 这样，Adobe就能够通过控制和维护发送、渲染和跟踪电子邮件促销活动所需的DNS的所有方面，将消息作为托管服务进行传送。

>[!NOTE]
>
>默认情况下，[!DNL Journey Optimizer]许可合同允许您最多委派10个子域。 如果要提高此限制，请联系您的Adobe联系人。
>
>Journey Optimizer当前不支持使用CNAME进行子域委派。

要委派新子域，请执行以下步骤：

1. 访问&#x200B;**[!UICONTROL Channels]** / **[!UICONTROL Subdomains]**&#x200B;菜单，然后单击&#x200B;**[!UICONTROL Delegate subdomain]**。

   ![](../assets/subdomain-delegate.png)

1. 指定要委派的子域的名称。

   ![](../assets/subdomain-name.png)

1. 此时将显示要放入您的 DNS 服务器中的记录列表。逐个复制这些记录，或者下载 CSV 文件，然后导航到您的域托管解决方案以生成匹配的 DNS 记录。

   确保所有DNS记录都已生成到您的域托管解决方案中。 如果一切配置正确，请选中“I confirm...”框，然后单击&#x200B;**[!UICONTROL Submit]**。

   ![](../assets/subdomain-submit.png)

   >[!NOTE]
   >
   >您稍后可以使用&#x200B;**[!UICONTROL Save as draft]**&#x200B;按钮创建记录并提交子域配置。 然后，您将能够从子域列表中打开子域委派，以恢复子域委派。

1. 提交子域委派后，该子域将显示在列表中，并且状态为&#x200B;**[!UICONTROL Processing]**。 有关子域状态的更多信息，请参阅[此部分](access-subdomains.md)。

   在验证子域之前，将执行以下检查和操作，并可用于发送消息。

   此步骤由Adobe执行，最长可能需要3小时。

   1. 检查子域是否已委派给AdobeDNS（NS记录、SOA记录、区域设置、所有权记录），
   1. 为域配置DNS，
   1. 创建跟踪和镜像URL，
   1. 配置CDN云前端、
   1. 创建、验证和附加CDN SSL证书，
   1. 创建转发DNS，
   1. 创建PTR记录。

   ![](../assets/subdomain-processing.png)

1. 检查成功后，子域将获得&#x200B;**[!UICONTROL Success]**&#x200B;状态。 它已准备好用于投放消息。

   <!-- later on, users will be notified in Pulse -->

   ![](../assets/subdomain-notification.png)


