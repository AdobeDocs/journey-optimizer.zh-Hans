---
name: ai-augmented-blocks
description: 为Adobe Journey Optimizer文档(journey-optimizer.en)生成并维护AI知识参考块。 当帮助/使用/下的新页面需要AI块时、当现有页面已更改并且其块可能漂移时，或者当要求添加/更新/验证AI知识引用（AI增强）内容时，使用。 在help/_include/do-not-localize/<folder>/ai-augmented-<page>.md下生成“不本地化include”，将其链接到包含{{$include}}的页面，运行强制的独立验证轮以便块是真实且明确的，在DOCAC JIRA任务中跟踪工作，并且（仅在询问作者之后）打开PR。 永远不要合并。
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '1124'
ht-degree: 0%

---


# AI知识参考块

此技能生成和维护的&#x200B;**AI知识引用**折叠面板块
Adobe Journey Optimizer文档(`journey-optimizer.en`)。 这些区块结构化，
附加到文档页面的非本地化上下文，以便AI Assistant回答以下问题
Journey Optimizer更加准确。

每个块都存储为&#x200B;**不本地化包含**（因此从不进行翻译）并提取
使用`{{$include}}`进入其页面。 块仅包含可从自身页面派生的事实&#x200B;**正文** — 未从其他页面、一般产品知识或HTML注释导入任何内容。

> **在生成任何内容之前读取引用文件。** 它们包含实际的规则，而不是
> 摘要：
> - `references/generation-spec.md` — 块结构，固定开口，逐段
>   内容规则和每个精度规则(硬限制与推荐限制、验证模式、
>   状态标签，无收缩，禁止单词列表)。
> - `references/verification-round.md` — **强制**独立对手事实检查
>   那是最后的质量关卡。 这不是可选操作，无法跳过。
> - `references/git-jira-tracking.md` — 分支/提交/PR流程(在打开
>   PR；**从不合并**)和DOCAC JIRA跟踪。

## 此技能适用时

- 在`help/using/<folder>/`下创建的&#x200B;**新页面**→为其生成块。
- **现有页面已更改**，→检查其块是否从页面正文偏移并进行更新。
- 要求您&#x200B;**添加、更新、验证或审核** AI知识引用/AI增强的块。

## 范围和排除项

- **范围：`help/using/<folder>/`下的**&#x200B;页。
- **超出范围 — 从不在此处添加块：**
  - `help/rp_landing_pages/` （入门/登陆页面） — 由作者规则排除。
  - 精简导航/链接中心、仅索引页面和几乎空的页面。 当页面为空页面时
    没有实质性概念的链接列表，**跳过它并说原因** — 不强制阻止阻止。
  - 发行说明（`help/using/rn/`，发行说明页面）。
- 当人们怀疑某个页面是否具有足够的实质内容时，从内容来判断：它是否具有真正的教育意义
概念、限制或术语涵盖它；如果它仅指向其他位置，则跳过它。

## 工作流

一次处理&#x200B;**一个文件夹（或一个页面）**。 不要将不相关的文件夹批处理到一个分支中。

### 1 — 确定目标和模式

询问作者（或从请求/打开的文件中推断）要处理的页面，并检测
每页模式：

- **CREATE** — 该页面没有`{{$include .../ai-augmented-<page>.md}}`行并且不存在
内联`+++ AI Knowledge Reference`块→生成新块。
- **UPDATE** — 该页面已具有块。 计算页面主体哈希并将其与
  包含同步评论中的`source-hash`（见下文）。 如果两者不同，则页面会漂移→
  重新生成/刷新块。 如果二者匹配，则该块为当前→跳过（报告“最新”）。
- **迁移** — 页面具有&#x200B;*内联* `+++ AI Knowledge Reference`块（尚未启用）
externalized)→将其移到“do-not-localize include”（请勿本地化）中，并使用 `{{$include}}`
行，保留内容保真度。

在任何地方都以相同的方式计算页面主体哈希（用于同步注释和漂移检查）：

```bash
md5 -q help/using/<folder>/<page>.md | cut -c1-8
```

在编辑页面&#x200B;**之前**计算它（哈希覆盖主体，就像块处于以下状态一样）
生成)。 在Linux上，使用`md5sum help/using/<folder>/<page>.md | cut -c1-8`。

### 2 — 生成（或刷新）块

每个页面完全关注`references/generation-spec.md`。 关键不变量：

- 两个&#x200B;**固定了打开的第**&#x200B;段，逐字，逐字节（从不转译）。
- 节顺序： **TL；DR；意图；术语表；护栏；术语；常见问题解答**。
- 每个声明都只以页体为基础。 没有收缩。 将数字限定为
  当页面使用强制/推荐时，`(hard limit)` / `(recommended)` **仅**
  措辞；否则不使用限定符。 使用页面的精确验证模式和状态标签。
  保留`[!UICONTROL ...]` / `[!DNL ...]`字符串。 不要使用禁止的不精确性
  术语，除非它们逐字显示在页面上。

**包含文件** — `help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md`
（如果需要，请创建`<folder>`子目录；使用`-`拼合任何嵌套页面路径）：

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening paragraphs + the six sections]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of the page body> -->
```

**页面编辑** — 只添加一行，作为最后一行内容，前面加一行空白
（请勿触摸页面中的其他内容）：

```
{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}
```

在更新时，仅编辑包含文件（如果您希望跟踪，请编辑`ai-section-version`）
修订版)；页面的`{{$include}}`行通常保持不变。 刷新`source-hash`至
块再次与页面匹配后当前的页面主体哈希。

在`references/generation-spec.md`中运行&#x200B;**自检**(步骤3 verify-every-claim +
生成后核对清单)。 这是2号门。

### 3 — 独立核查回合（强制性最后关口）

这是作者特别要求的步骤：**确认每个块有效、为true，并且
无二义性。** 以&#x200B;*新增、独立的*传递方式运行 — 最好是单独的子代理
只查看页面正文和块，不记忆块是如何写入的 — 如下
`references/verification-round.md`. 它会重新检查所有索赔，降低任何标示错误的限制，
修复了同义词vs-Do-Not-confusion错误，并删除页面中不接地的所有内容。 应用
每次修复都包含文件，然后再继续。 这是2的入口2，不能跳过。

### 4 — 结构扫描

在提交之前，请扫描每个块以检查结构和卫生（请参见中的扫描片段）
`references/git-jira-tracking.md`)：前置内容+ `# AI Knowledge Reference`标题，
`+++ … +++`栅栏，固定开头的段落，同步注释，无收缩(不包括
逐字`[!UICONTROL ...]`)，以及页面中匹配的`{{$include}}`行。

### 5 — 在JIRA中跟踪，然后询问PR（从不合并）

关注`references/git-jira-tracking.md`：

1. 提交针对JIRA任务(`DOCAC-<key>`)的名为的分支，从不提交`main`。 验证
承诺登陆分支（在`origin/main`之前提交1次），而不是在`main`上。
2. 更新DOCAC任务：使用更改的内容进行注释+验证结果，设置修复
版本，并根据您团队的流程要求对其进行转换。
3. **询问作者是否想要拉取请求。** 只要他们同意就开一张。
4. **从不合并。** 这些PR是供人工审阅的；合并始终是作者的调用。

### 6 — 报表

每页报告：已创建/更新/已迁移/已跳过（+原因），验证结果
（清理或更正，并进行更正）、JIRA任务以及PR链接（如果已打开）。

## 有关运行该技能的作者的备注

- 块是某个时间点页面主体的&#x200B;**派生** — 将其视为
页面。 当您以接触护栏、限制、状态标签或的方式更改页面时
验证模式，在同一更改中更新块。
- JIRA和PR步骤需要访问公司JIRA和GitHub。 如果你没有
访问，仍生成+验证块并在本地打开更改；提交JIRA/PR步骤
给有这种想法的人。
- 此技能存在于存储库中，因此整个编写团队共享一个过程。 改进
在此处引用文件，而不是保留专用副本。
