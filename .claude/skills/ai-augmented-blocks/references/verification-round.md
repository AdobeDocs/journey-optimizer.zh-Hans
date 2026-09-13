---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---
# 验证轮 — 强制性最终质量关卡

这是2的入口2，并且保证每个块的步骤为&#x200B;**有效、为真且为自由
二义性**。 它是&#x200B;**非可选内容，不能跳过**，包括单页更新。

## 为什么是独立的

块作者（门1）离块太近，无法捕获自己的接地错误。 门2
是**独立的对手重新检查**：新审核者假定该块可能错误
并尝试使用**only**&#x200B;页面正文作为真值来证明它。 将其作为&#x200B;**独立的子代理运行**
这还没看过街区是怎么写的 — 这种独立性才使它变得有效。 对象
一整批页面，一个验证子代理可以覆盖整个文件夹。

## 验证器的作用（每页）

1. 读取&#x200B;**完整源页面** `help/using/<folder>/<page>.md`。 HTML-comment /
注释掉的内容是**非**&#x200B;有效的源。
2. 读取&#x200B;**块** `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`。
3. 将&#x200B;**every**&#x200B;声明分类为BEARDED / UNACTIVE / NOT-BEARDED （针对页面正文）。
4. **通过仅编辑块文件修复每个问题** — 保留两个已修复的打开部分
段落、`+++ … +++`栏和同步注释。 切勿修改源页面。
5. 每页报告： `clean`或`N issues` +应用的确切修复。

## 对抗清单（首先列出风险最高的项目）

- **数字和限制。** 每个值都精确。 仅当页面使用时才限制为`(hard limit)`
强制/最大措辞；`(default)`（如果可用/默认/可配置，包括“请求”）
（通过您的Adobe代表获得更多信息）或“通过API获得价值”)；`(recommended)`以获取建议；否
限定符（如果页面未提供任何内容）。 **将生成器上标为hard的任意上限降级。**
每个吞吐量/速率数字都包含其范围。
- **日期、ID、产品/字段名称、SQL标识符、状态枚举、错误字符串** — 逐字
页面上的。 对法规遵从性/法律时限的零容忍：从不发明SLA、保留、
或执行日期；将任何日期与页面声明的日期完全一致，并标记为页面
为其设置框架。
- **同义词与不要混淆。** 同义词(`"A" = "B"`)需要页面上的两个表单
意思是一样的。 任何对比度(`"X" ≠ "Y"`)都属于“请勿混淆”下。 移动
标签错误。
- **验证/测试模式**使用页面的确切术语命名，没有混淆
经典vs — 重新设计的体验或跨渠道。
- **接地。** 没有从其他页面、一般产品知识或HTML导入任何内容
注释。 移除页面正文不支持的内容。
- **样式。** 无收缩（在逐字`[!UICONTROL ...]` / `[!DNL ...]`字符串之外）。 无
禁止使用的单词（“合成”、“虚假数据”、“没有真实数据”、“还原”、“回滚”）
除非在页面上一字不差。 UI字符串完全保留。
- **结构。** 开头的两个段落完整而一字不差；有六个段落在开头，在开头
页面支持它们的顺序；存在同步注释。

## 可重复使用的验证程序子代理提示

填写文件夹和页面列表。 将其作为独立的通用子代理启动。

```
You are an ADVERSARIAL fact-checker for Adobe Journey Optimizer doc "AI Knowledge Reference"
blocks. Repo: <repo path>. Assume each block MAY contain errors; try hard to find them. This is
the final accuracy gate.

PAGES (basenames): <p1> <p2> ...
SOURCE: help/using/<folder>/<p>.md   BLOCK: help/_includes/do-not-localize/<folder>/ai-augmented-<p>.md

For EACH page:
1. Read the FULL source page body (HTML-comment / commented-out content is NOT valid source).
2. Read the block.
3. Classify EVERY claim GROUNDED / INACCURATE / NOT-GROUNDED against the page body. Scrutinize:
   numeric limits (hard only if the page uses enforcement/maximum wording; downgrade any
   raisable/default/configurable value the block marked hard; every rate figure needs its
   scope); dates/IDs/field names/SQL identifiers/status enums/error strings verbatim and no
   invented SLA/legal timeframes; Synonyms are true equivalents (mislabels -> Do not confuse);
   validation/test modes named with the page's exact terms and not conflated; nothing imported
   from other pages or HTML comments; no contractions (outside verbatim [!UICONTROL ...]); no
   banned words (synthetic / fake data / without real data / revert / roll back) unless verbatim.
4. FIX every issue by editing ONLY the block file. Preserve the two fixed opening paragraphs,
   the +++ ... +++ fences, and the sync comment. Do NOT modify source pages.

Report per page: "<p>: clean" or "<p>: N issues" + the exact fixes applied.
```

## 退出标准

仅当验证器将每个页面报告为`clean`时，文件夹才会通过入口2（它找到了任一页面）
什么也没有，或者它进行了修复，而现在块是干净的)。 如果应用了修复，则它们已经是
在块文件中 — 将其包含在最终报告中，然后继续扫描并提交。
