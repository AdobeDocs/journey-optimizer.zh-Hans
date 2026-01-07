---
solution: Journey Optimizer
product: Journey Optimizer
title: 预览和测试内容
description: 在启动之前验证消息的准确性。 使用测试用户档案预览个性化内容、向利益相关者发送验证、检查跨客户端的电子邮件渲染、评估垃圾邮件分数和有效测试多个内容变体。
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 23%

---

# 预览和测试内容{#section-overview}

>[!BEGINSHADEBOX]

**用途：**&#x200B;营销活动和历程的启动前验证工具\
**主要用户：**&#x200B;营销活动经理、电子邮件营销人员、内容创建者\
**关键结果：**&#x200B;客户交付前发生Catch错误

>[!ENDSHADEBOX]

通过在错误到达客户之前捕获错误，确保无懈可击的消息传递。 预览内容会验证不同客户配置文件中的个性化准确性，而测试工具会揭示可能影响参与度的呈现问题、垃圾邮件风险和内容变体。 访问全面的功能以将验证发送给利益相关者，使用示例数据模拟个性化，检查跨客户端的电子邮件渲染并评估可投放性指标 — 所有这些都在激活之前。 掌握这些验证技术可保护品牌声誉、最大化收件箱放置并持续提供出色的客户体验。

## 预览和测试内容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg?lang=zh-Hans)

如何预览和测试您的内容

了解如何使用测试用户档案和样本输入数据来预览和测试内容、发送校样并确保个性化准确性。

[预览和测试入门](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg?lang=zh-Hans)

如何选择测试配置文件

了解如何选择和管理测试用户档案，以便有效地预览和测试个性化内容。

[了解如何选择测试用户档案](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg?lang=zh-Hans)

使用测试用户档案预览您的内容

使用测试用户档案预览个性化内容及模拟内容变体的分步指南。

[使用测试用户档案预览内容](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg?lang=zh-Hans)

使用测试用户档案数据发送校样

使用测试用户档案数据发送校样来测试和验证电子邮件，以确保内容的准确性。

[了解如何发送校样](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg?lang=zh-Hans)

如何使用Litmus测试电子邮件渲染

集成 Litmus，预览电子邮件在各主流邮件客户端中的渲染效果，确保显示正常。

[使用 Litmus 测试电子邮件渲染效果](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg?lang=zh-Hans)

如何模拟和测试内容变体

使用样本输入数据模拟内容变体，以测试个性化内容并确保准确性。

[模拟内容变体](../using/test-approve/simulate-sample-input.md)
:::

::::

## 快速决策指南

**上下文：**&#x200B;此表将测试目标映射到Adobe Journey Optimizer中的特定工具。

根据您的目标选择测试方法：

| **如果您需要……** | **使用此工具** |
|----------------------|-------------------|
| 验证个性化是否正确显示 | [测试用户档案](../using/content-management/test-profiles.md) |
| 快速测试10个以上的内容变体 | [示例输入数据](../using/test-approve/simulate-sample-input.md) |
| 发送前获得利益相关者的批准 | [发送校样](../using/content-management/proofs.md) |
| 检查Gmail、Outlook、Apple Mail中的电子邮件显示 | [Litmus渲染](../using/content-management/rendering.md) |
| 改进收件箱放置 | [垃圾邮件报告](../using/content-management/spam-report.md) |
| 一次预览所有变体 | [预览模式](../using/content-management/preview.md) |

## 测试工作流核对清单

**上下文：**&#x200B;建议的5步测试序列适用于所有渠道（电子邮件、短信、推送、Web、应用程序内）。

按照以下顺序进行综合验证：

1. **预览** — 使用测试配置文件正确检查个性化渲染
2. **测试变体** — 上传示例数据CSV/JSON以验证多个方案
3. **检查可投放性**（电子邮件） — 运行垃圾邮件报告和渲染测试
4. **发送校样** — 与利益相关者共享以供审阅和批准
5. **最终检查** — 验证所有链接、图像和CTA是否正常工作

**专业提示：**&#x200B;测试至少3个代表不同客户区段（高值、新、非活动）的用户档案，以捕获边缘案例。

## 常见方案

**上下文：**&#x200B;显示如何在典型用例中应用测试工具的真实示例。

**场景1：测试多区段营销活动的个性化电子邮件**
→使用[示例输入数据](../using/test-approve/simulate-sample-input.md)测试20-30个变体，而不创建单独的测试配置文件。 上传具有不同客户属性的CSV并一次预览所有内容。

**场景2：在主发送之前验证电子邮件渲染**
→运行[Litmus测试](../using/content-management/rendering.md)以检查跨顶级电子邮件客户端的显示情况，然后检查[垃圾邮件报告](../using/content-management/spam-report.md)以确保收件箱的位置。

**场景3：获取利益相关者签发**
→[将校样](../using/content-management/proofs.md)发送给内部审阅人，其中包含测试配置文件数据，以便他们能够准确地看到客户将收到的内容。

## 主要要点

- **测试用户档案**&#x200B;对于预览个性化内容至关重要；请使用示例输入数据高效地测试10个以上的变体
- **特定于电子邮件的工具**&#x200B;包括渲染测试(Litmus)、垃圾邮件报告和验证
- **建议的序列：**&#x200B;预览→测试变体→检查可投放性→发送验证→最终检查
- **节省时间：**&#x200B;上传具有客户属性的CSV/JSON，而不是创建单独的测试配置文件

## 其他资源

- **[如何使用电子邮件垃圾邮件报告](../using/content-management/spam-report.md)** — 使用垃圾邮件报告功能评估电子邮件内容的垃圾邮件分数，以提高可投放性。

**相关主题：** [测试和批准登陆页面](test-landing-page.md) | [审批工作流](approve-landing-page.md) | [正在创建测试用户档案](../using/audience/creating-test-profiles.md)
