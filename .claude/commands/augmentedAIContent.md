---
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 3%

---
# augmentedAIContent

在Journey Optimizer文档存储库中的一个或多个标记文件的末尾附加自动生成的AI助手折叠面板。

## 目标存储库

`help/using/` （相对于存储库根）

## 可折叠项语法(Experience League)

```
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**规则：**
- 一行中有`+++Title` — 标题紧跟`+++`
- 仅`+++`在一行中关闭折叠面板
- 开始`+++`之前和结束`+++`之后的空白行

---

## 工作流

### 步骤1 — 询问目标

询问用户：
> 您要扩充哪个文件或文件夹？
> - 单个文件：相对于存储库根目录的路径（如`help/using/email/get-started-email.md`）
> - 文件夹：所有`.md`文件都是递归的（如`help/using/email`）
> - 文件/文件夹列表

如果提供了文件夹，请列出找到的`.md`文件，并在处理之前进行确认。

### 步骤2 — 对于每个文件：读取和生成

1. **完整读取文件**。
2. **了解页面主题** — 它涵盖什么功能、概念或任务？
3. **使用以下规则生成折叠内容**。
4. **检查**&#x200B;末尾是否存在AI折叠面板（查找末尾附近的`+++AI Assistant`）。 如果是，询问用户：替换还是跳过？

### 步骤3 — 附加折叠

在文件末尾附加。 请勿修改任何其他内容。

### 第4步 — 报表

- 修改的文件✓
- 跳过的文件+原因（已有可折叠项/空/索引页）

---

## 内容生成规则

分析页面并按&#x200B;**的顺序生成以下**&#x200B;部分作为Markdown项目符号列表。 跳过无法提取任何有意义内容的部分。

### 可折叠项标题

`+++AI Assistant — Page context`

### &#x200B;1. TL；DR

一句概括了页面的教程或功能。

```
- **TL;DR:** [one sentence]
```

### &#x200B;2. 意图

阅读本页后，用户可以完成3-6件事。

```
**Intents:**
- [action]
- [action]
```

### &#x200B;3. 术语表

此页面/功能的特定关键术语，带有简短定义。 标记特定于产品的术语。

```
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
```

仅包含与此页面相关的术语。 不要使用通用的营销词语进行填充。

### &#x200B;4. 护栏

页面上提到的限制、先决条件、权限或限制。

```
**Guardrails:**
- [guardrail]
```

### &#x200B;5. 术语

规范名称、缩写、接受的变体、同义词、消除歧义。 主要用于AI管道标准化。

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

### &#x200B;6. 常见问题

用户可能会问3到6个问题，并提供简短答案。

```
**FAQ:**
- **Q: [question]** — [short answer]
```

### 不应包含的内容

- 请&#x200B;**不**&#x200B;重写或摘要正文内容（该内容已在页面中）
- 请&#x200B;**不**&#x200B;包含分步说明
- 不要&#x200B;**创建该页面不支持的内容**

### 完整模板

```markdown
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

---

## 注释

- 逐个处理文件以提高质量。
- 标记非常短或仅用于索引的页面，并询问用户是否跳过。
- 不创建新文件 — 仅编辑现有`.md`文件。
