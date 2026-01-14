---
solution: Journey Optimizer
product: Journey Optimizer
title: 预览和测试内容
description: 发布前请核实消息准确性。使用测试轮廓预览个性化内容，向利益相关者发送校样，检查邮件在各客户端的渲染效果，评估垃圾邮件评分，并高效测试多种内容变体。
redpen-status: CREATED_||_2025-08-11_20-30-05
exl-id: bd78e0af-573b-4880-a9f1-44467c9db159
source-git-commit: 6b83b015dfd74da9eb58bd06958d0963d81c6489
workflow-type: ht
source-wordcount: '657'
ht-degree: 100%

---

# 预览和测试内容{#section-overview}

>[!BEGINSHADEBOX]

**用途：**&#x200B;为营销活动与历程提供发布前验证工具\
**主要用户：**&#x200B;营销活动管理员、电子邮件营销人员、内容创作者\
**关键结果：**&#x200B;在触达客户前发现并纠正错误

>[!ENDSHADEBOX]

在触达客户前发现并纠正错误，确保信息传递准确无误。预览功能可验证不同客户轮廓间的个性化内容准确性，测试工具则能揭示可能影响参与度的渲染问题、垃圾邮件风险及内容变体差异。借助综合全面的功能，在激活内容前执行以下操作：向利益相关者发送校样、通过样本数据模拟个性化效果、检查邮件在各客户端的呈现情况，并评估邮件送达率指标。掌握这些验证方法，以维护品牌声誉、优化收件箱抵达率，并持续提供卓越的客户体验。

## 预览和测试内容

:::: landing-cards-container
:::
![icon](https://cdn.experienceleague.adobe.com/icons/circle-play.svg)

如何预览和测试内容

了解如何使用测试用户档案和样本输入数据来预览和测试内容、发送校样并确保个性化准确性。

[预览和测试入门](../using/content-management/preview-test.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/list-check.svg)

如何选择测试轮廓

了解如何选择和管理测试用户档案，以便有效地预览和测试个性化内容。

[了解如何选择测试用户档案](../using/content-management/test-profiles.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/bullseye.svg)

使用测试用户档案预览您的内容

使用测试用户档案预览个性化内容及模拟内容变体的分步指南。

[使用测试用户档案预览内容](../using/content-management/preview.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/envelope.svg)

使用测试用户档案数据发送校样

使用测试用户档案数据发送校样来测试和验证电子邮件，以确保内容的准确性。

[了解如何发送校样](../using/content-management/proofs.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/eye.svg)

如何使用 Litmus 测试电子邮件渲染效果

集成 Litmus，预览电子邮件在各主流邮件客户端中的渲染效果，确保显示正常。

[使用 Litmus 测试电子邮件渲染效果](../using/content-management/rendering.md)
:::

:::
![icon](https://cdn.experienceleague.adobe.com/icons/code-branch.svg)

如何模拟和测试内容变体

使用样本输入数据模拟内容变体，以测试个性化内容并确保准确性。

[模拟内容变体](../using/test-approve/simulate-sample-input.md)
:::

::::

## 快速决策指南

**使用场景：**&#x200B;此表格将测试目标与 Adobe Journey Optimizer 中的具体工具进行对应。

根据您的目标选择测试方法：

| **如果您需要……** | **使用此工具** |
|----------------------|-------------------|
| 验证个性化内容是否准确显示 | [测试轮廓](../using/content-management/test-profiles.md) |
| 快速测试 10 个以上的内容变体 | [示例输入数据](../using/test-approve/simulate-sample-input.md) |
| 发送前获得利益相关者的批准 | [发送校样](../using/content-management/proofs.md) |
| 检查电子邮件在 Gmail、Outlook、Apple Mail 中的显示效果 | [Litmus 渲染](../using/content-management/rendering.md) |
| 提升收件箱抵达率 | [垃圾邮件报告](../using/content-management/spam-report.md) |
| 一次预览所有变体 | [预览模式](../using/content-management/preview.md) |

## 测试工作流核对清单

**使用场景：**&#x200B;适用于所有渠道（电子邮件、短信、推送、Web、应用程序内）的推荐的五步测试流程。

按照以下流程进行全面验证：

1. **预览** - 使用测试轮廓检查个性化内容渲染准确性
2. **测试内容变体** - 上传示例数据 CSV/JSON 以验证多个场景
3. **检查送达率**（电子邮件）- 执行垃圾邮件报告与渲染测试
4. **发送校样** - 与利益相关者共享以供审阅和批准
5. **最终检查** - 确认所有链接、图片及行动号召按钮运作正常

**专业建议：**&#x200B;使用至少 3 类代表不同客户分群（高价值用户、新用户、非活动用户）的轮廓进行测试，以覆盖边缘情况。

## 常见应用场景

**使用场景：**&#x200B;通过真实案例展示如何在典型用例中应用测试工具。

**场景一：测试多细分群体营销活动的个性化邮件**
→ 使用[样本输入数据](../using/test-approve/simulate-sample-input.md)一次性测试 20-30 种变体，无需单独创建测试轮廓。上传包含不同客户属性的 CSV 文件，即可批量预览所有变体。

**场景二：在大规模发送前验证邮件渲染**
→ 运行 [Litmus 测试](../using/content-management/rendering.md)以检查在主流邮件客户端上的显示效果，随后检查[垃圾邮件报告](../using/content-management/spam-report.md)以确保收件箱抵达率。

**场景三：获取利益相关者审批确认**
→ 通过[发送校样](../using/content-management/proofs.md)（包含测试轮廓数据）给内部审核人员，使其能准确看到客户将收到的内容。

## 关键要点

- **测试轮廓**&#x200B;是预览个性化内容的关键工具；使用样本输入数据可高效测试 10 种以上内容变体
- **电子邮件专项工具**&#x200B;包含渲染测试 (Litmus)、垃圾邮件报告和校样
- **推荐序列：**&#x200B;预览 → 测试内容变体 → 检查送达率 → 发送校样 → 最终检查
- **效率提升技巧：**&#x200B;上传含客户属性的 CSV/JSON 文件，无需单独创建测试轮廓

## 其他资源

- **[如何使用电子邮件垃圾邮件报告](../using/content-management/spam-report.md)** - 使用垃圾邮件报告功能评估邮件内容的垃圾邮件评分，从而提升可投放性。

**相关主题：**[测试和批准登陆页面](test-landing-page.md) | [审批工作流](approve-landing-page.md) | [创建测试轮廓](../using/audience/creating-test-profiles.md)
