---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '846'
ht-degree: 4%

---
# 生成规范 — AI知识参考块

AI知识参考块包含的内容及其原理的单一真实来源
书面。 完全按照每个页面进行操作。 (这反映了旧版
`.claude/commands/augmentedAIContent.md`；技能是规范版本。)

## 黄金法则

块只能包含&#x200B;**从其自身页面正文派生的内容。** 不是其他页面，不是
是一般产品知识，而不是HTML注释的/注释掉的内容。 如果页面未显示
这个街区也没有。

## 可折叠项+包含语法

```
+++ AI Knowledge Reference

Content here — standard markdown.

+++
```

- `+++ AI Knowledge Reference`打开（`+++`后一个空格）；仅`+++`关闭。
- 开始`+++`之前和结束`+++`之后的空白行。
- 标题始终恰好为`AI Knowledge Reference`。
- 整个手风琴都生活在非本地化的包中，页面会把它拉进来
  `{{$include /help/_includes/do-not-localize/<folder>/ai-augmented-<page>.md}}`. 下的内容
  `help/_includes/do-not-localize/`被排除在本地化之外 — 这就是块的保留方式
  未翻译。

## 包含文件结构

```
---
title: AI Knowledge Reference
---
# AI Knowledge Reference

+++ AI Knowledge Reference

[fixed opening — verbatim]

[the six sections in order]

+++

<!-- ai-section-version: 1 | source-hash: <first 8 chars of md5 of page body> -->
```

- **文件名：**&#x200B;派生自相对于其顶级的页面路径 `help/using/<folder>/`
节：删除`.md`，将任何剩余的`/`替换为`-`，前缀为`ai-augmented-`。
  - `help/using/building-journeys/end-journey.md` → `ai-augmented-end-journey.md`
  - `help/using/building-journeys/expression/journey-properties.md`→
    `ai-augmented-expression-journey-properties.md`
- 每个顶级节(`building-journeys/`、`email/`、`data/`、...)有一个子文件夹。

## 固定打开 — 逐字，从不修改

每个区段都以这两个段落开始。 逐字节复制；请勿转译，
压缩或重新排序：

```
This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

## 六个部分，按顺序排列

仅当页面没有为其生成有意义的内容时，才跳过部分。

### &#x200B;1. TL；DR
一句话：页面教授或启用的内容。`* **TL;DR:** [one sentence]`

### &#x200B;2. 意图
用户在阅读页面后可以完成3-6件事。

### &#x200B;3. 术语表
具有简短定义的特定于页面的关键术语；将产品特定的术语标记为
`*(product-specific)*`. 没有通用的营销填充。

如果页面包含测试/预览/模拟，则&#x200B;**验证模式精度（必需）：**
执行，区分页面实际名称的每个模式 — 不要折叠它们。 请使用
页面的确切术语(例如`Simulate content`、`Simulate content (AEP profiles)`、
`Send proof`, `Test mode`, `Dry run`, `Simulation`, `test profile`, `sample input`). 从不
将“合成用户档案”、“虚假数据”或“没有真实数据”替换为其中的任何一个。

### &#x200B;4. 护栏
页面上所述的限制、先决条件、权限和限制。

- **将每个数字限制**&#x200B;限定为`(hard limit)`或`(recommended)` — 但&#x200B;**仅**当
页面使用强制措辞（错误/已拒绝/最大/不能超过/仅限……支持）
或推荐用语（为获得最佳性能/推荐）。 如果页面未提供
限定词，不提供。 **绝不要将可产生、默认或可配置的值标记为硬值。**
可以通过“联系您的Adobe代表”或通过API提升的值包括
  `(default)`，不硬。
- **将每个吞吐量/速率数字限定为其范围**（每个沙盒/每个组织/每个实例）。
- **对照页面正文交叉检查每个数字。** 页面正文具有权威性。
- **不推断**页面未显示的护栏。 无元注释(“页面不
指定……”)。

### &#x200B;5. 术语
规范名称、缩写、变体、同义词、消除歧义。

- **同义词** (`"A" = "B"`)仅适用于&#x200B;**true等同项** — 这两个表单都必须显示在页面上
意思是一样的。 任何具有*对比度*&#x200B;且低于&#x200B;**的对比度，请勿混淆**
(`"X" ≠ "Y"`)，不是同义词。
- **状态/生命周期精度：**从页面正文中复制确切的状态标签；不复制
转述。 使用“请勿混淆”来分隔共享根单词的状态。

### &#x200B;6. 常见问题
可能有3-6个问题需要回答较短的答案。 答案使用与页面&#x200B;**相同的动词和名词
正文**。 除非页面使用，否则不要引入“还原”、“重置”或“回滚”。

## 不应包含的内容

- 请勿重写或总结正文内容，或提供分步说明。
- 不要创作页面不支持的内容。
- 除非这些术语在页面上显示为&#x200B;**逐字**，否则请不要使用这些不精确的术语：
“合成”、“虚假数据”、“没有真实数据”、“还原”、“回滚”。
- **无收缩**在区块散文中的任何位置 — 拼出“不是”、“不是”、“不能”、
&quot;it is&quot;等。(唯一的例外是逐字产品UI字符串，例如
  `[!UICONTROL configuration doesn't exist]`，将完全保留。)

## 第3步 — 核实每一项索赔（自查，第1门）

在写入include之前，通过声明重新读取生成的内容声明。 强制，即使对于
短页。 在写入之前更正任何故障，并在报告中记录更正情况。

- 块中的每个术语/标签/UI名称都会显示在页面主体中。
- 没有同义词，除非两个表单都出现在页面上；每个“请勿混淆”仅引用
此页面上的概念。
- 每个数值都与页正文完全匹配；每个限制限定符都由
页上的用词，没有发明的限定词。
- 没有从其他页面或一般知识导入的词汇表/常见问题解答详细信息。
- 除非在页面上一字不差，否则不得使用被禁止的不精确术语；不得使用缩写。

## 生成后核对表（1号门，续）

- [ ]每个数值都逐字存在/可从页面正文中派生。
- [ ]每个限制都正确限定（硬限制与建议限制与无限制）；没有默认/可raisable值
 标签错贴了。
- [ ]每个吞吐量数字都有其范围。
- [ ]页面上存在的所有验证模式都使用与页面精确相关的术语进行命名。
- [ ]所有生命周期状态都使用精确的页面标签。
- [ ]同义词为True等同项；对比位于“Do not confuse”下。
- [ ]没有禁止的单词/没有收缩（在逐字UI字符串之外）。
- [ ]词汇表没有通用术语；常见问题解答不引入页面中不存在的任何内容。

1号门是检查自己作品的编写者。 它&#x200B;**不**替换
`verification-round.md`中的独立验证轮（门2）。
