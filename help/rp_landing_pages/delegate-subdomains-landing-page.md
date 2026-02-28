---
solution: Journey Optimizer
product: Journey Optimizer
title: 委派电子邮件子域
description: 委派电子邮件子域
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: bb50d06e86f9399dfd295b8091aa637abcaea4a8
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 41%

---

# 委派电子邮件子域{#section-overview}

委派电子邮件子域是[渠道配置](../using/configuration/get-started-configuration.md)中的核心步骤 — 在从Journey Optimizer发送电子邮件之前是必需的。 子域允许您隔离流量类型（例如，营销型与事务型），保护主域的信誉，并加快[IP预热速度](../using/configuration/ip-warmup-gs.md)。 它们与[电子邮件通道配置](../using/email/get-started-email-config.md)和[可投放性监控](../using/reports/deliverability.md)配合使用，以确保邮件到达收件箱。

您可以从多种设置方法中进行选择：**完全委派** (Adobe管理DNS)、**CNAME设置**&#x200B;或&#x200B;**自定义委派** （您拥有证书和DNS）。 如果您开始使用CNAME，则可以稍后进行[迁移到自定义委派](../using/configuration/custom-subdomain-migration.md)，以获得更严格的安全性。 此部分还介绍了DMARC和PTR记录、Gmail的Google TXT记录以及IP池。 有关更宽泛的可交付性指导，请参阅[可交付性入门](../using/reports/deliverability.md)和[监视电子邮件地址](monitor-reputation-landing-page.md)。

## 委派电子邮件子域

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

子域委派快速入门

了解在 Adobe Journey Optimizer 中委派子域的优势、配置方法和注意事项。

[开始委派子域](../using/configuration/about-subdomain-delegation.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/gear.svg?lang=zh-Hans)

委派子域

有关将子域委派到 Adobe 的分步指南，包括完全委派和 CNAME 设置。

[了解如何委派](../using/configuration/delegate-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/screwdriver-wrench.svg?lang=zh-Hans)

设置自定义子域

通过自定义委派获得子域的完全所有权 — 上传您自己的SSL证书并保持对域配置的完全控制。

[设置自定义子域](../using/configuration/delegate-custom-subdomain.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/chart-line.svg?lang=zh-Hans)

从CNAME迁移到自定义委派

将现有CNAME配置的子域迁移到自定义委派，以满足安全策略并获得对证书的完全控制。

[迁移子域](../using/configuration/custom-subdomain-migration.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/shield-halved.svg?lang=zh-Hans)

设置 DMARC 记录

配置 DMARC 记录以增强委派子域的电子邮件安全性和可投放性。

[立即设置 DMARC](../using/configuration/dmarc-record.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

添加 Google TXT 记录

通过在 Adobe Journey Optimizer 中添加 Google TXT 记录来验证子域，以提高 Gmail 可投放性。

[添加 Google TXT 记录](../using/configuration/google-txt.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

访问和编辑 PTR 记录

管理已委派子域的 PTR 记录，包括编辑和了解更新状态。

[编辑 PTR 记录](../using/configuration/ptr-records.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

创建 IP 池

对 IP 地址进行分组可提升电子邮件的可投放性，并有效管理子域信誉。

[创建 IP 池](../using/configuration/ip-pools.md)
:::

::::

## 其他资源

- **[配置登陆页面子域](../using/landing-pages/lp-subdomains.md)** — 为登陆页面和订阅表单设置子域。
- **[配置Web子域](../using/web/web-delegated-subdomains.md)** — 委派子域以进行Web体验和跟踪。
- **[渠道配置入门](../using/configuration/get-started-configuration.md)** — 所有渠道设置步骤（包括子域委派）的概述。
