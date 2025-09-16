---
solution: Journey Optimizer
product: Journey Optimizer
title: 委派电子邮件子域
description: 委派电子邮件子域
redpen-status: CREATED_||_2025-08-11_21-07-51
exl-id: 7df9b8e2-136a-4ffc-9243-53c7be026d81
source-git-commit: 2b907a3be8b11ac6308d0b563e122c88478d1d37
workflow-type: ht
source-wordcount: '244'
ht-degree: 100%

---

# 委派电子邮件子域{#section-overview}

在 Adobe Journey Optimizer 中委派电子邮件子域使管理员能够改进电子邮件可投放性、保护域信誉并简化活动管理流程。通过设置子域，您可以隔离不同类型的电子邮件流量，如营销和交易型消息，同时确保符合行业标准。本节将介绍关键配置方法（如完全委派和 CNAME 设置），并分析其在实施难度与控制权限方面的差异。您还将学习管理 DMARC 和 PTR 等核心 DNS 记录，通过 Google TXT 记录提升 Gmail 可投放性，以及使用 IP 池进行 IP 分组。无论是优化安全性还是维护信誉，本指南都将使整个过程变得简单高效。

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
