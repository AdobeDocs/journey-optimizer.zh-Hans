---
name: ajo-ai-accordion
description: 通过在每个Markdown文件末尾附加一个AI助手折叠部分，丰富Adobe Journey Optimizer文档页面。 读取每个页面，根据页面主题自动生成相关的AI助手内容，并将其插入为可折叠折叠折叠面板。 当用户想要将AI信息添加到AJO文档、通过AI内容扩充AJO Markdown页面或通过AI折叠面板部分处理Markdown文件的文件或文件夹时使用。
disable-model-invocation: true
source-git-commit: 80e67d5a60b6427ff87e106e37bf6794ac76a210
workflow-type: tm+mt
source-wordcount: '565'
ht-degree: 1%

---


# AJO AI折叠面板扩充

在Journey Optimizer文档存储库中的一个或多个标记文件的末尾附加自动生成的AI助手折叠面板。

## 目标存储库

`/Users/sauviat/GitHub/GHEC/journey-optimizer.en/help/using/`

## 可折叠项语法(Experience League)

```markdown
+++Title of the accordion

Content here — any standard markdown is valid.

+++
```

**规则：**
- 一行中有`+++Title` — 标题紧跟`+++`，中间没有空格
- 仅`+++`在一行中关闭折叠面板
- 开始`+++`之前和结束`+++`之后的空白行

&#x200B;---

## 工作流

### 步骤1 — 询问目标

询问用户：

> 您要扩充哪个文件或文件夹？
> - 单个文件：相对于存储库根目录的路径（如`help/using/email/get-started-email.md`）
> - 文件夹：递归处理内部的所有`.md`文件（例如`help/using/email`）
> - 文件/文件夹列表

使用`AskQuestion`（如果可用），否则按会话方式询问。

如果提供了文件夹，请列出找到的所有`.md`文件，并在处理之前与用户确认。

### 步骤2 — 对于每个文件：读取和生成

对于每个目标文件：

1. **完整读取文件**。
2. **了解页面主题** — 它涵盖什么功能、概念或任务？
3. **使用以下内容生成规则生成折叠内容**。
4. **检查**&#x200B;文件末尾是否存在AI折叠项（查找末尾附近的`+++`）。 如果是这样，请询问用户是更换还是跳过。

### 步骤3 — 附加折叠

在文件末尾附加：

```markdown
+++[ACCORDION_TITLE]

[GENERATED_CONTENT]

+++
```

不应修改文件中的其他内容。

### 第4步 — 报表

处理完所有文件后：
- 列出修改的文件✓
- 列出跳过的文件和原因（已有可折叠项、空文件、不相关等）

&#x200B;---

## 内容生成规则

通过分析Markdown页面生成折叠面板内容。 按&#x200B;**的顺序生成以下部分**，格式为Markdown项目符号列表。 跳过无法从页面中提取任何有意义内容的部分。

&#x200B;---

### 可折叠项标题

使用： `+++AI Assistant — Page context`

&#x200B;---

### 要生成的部分（按顺序）

**1. TL；DR**

一句话。 此页面会教授或启用哪些内容？

```markdown
- **TL;DR:** [one sentence summary]
```

&#x200B;---

**2. 意图**

用户在阅读本页后可以完成的任务项目符号列表（3-6项）。

```markdown
**Intents:**
- [action the user can perform]
- [action the user can perform]
```

&#x200B;---

**3. 词汇表**

特定于此页面/功能的关键术语，其定义简短。 标记特定于产品的术语。

```markdown
**Glossary:**
- **[Term]**: [definition] *(product-specific)*
- **[Term]**: [definition]
```

仅包含与此页面主题相关的术语。 不要使用通用的营销词语进行填充。

&#x200B;---

**4. 护栏**

页面上提到的限制、先决条件、权限或限制。

```markdown
**Guardrails:**
- [guardrail or prerequisite]
- [guardrail or prerequisite]
```

&#x200B;---

**5. 术语**

规范产品名称、首字母缩略词、接受的变体、同义词和消歧提示。 本节主要介绍AI管道标准化。

```markdown
**Terminology:**
- Canonical name: [e.g. Adobe Journey Optimizer]
- Acronym: [e.g. AJO] — variants: [e.g. Journey Optimizer, A-JO]
- Synonyms: [e.g. "brand guidelines" = "brand rules", "branding standards"]
- Do not confuse: [e.g. "AI Assistant" ≠ "Adobe Sensei"]
```

仅包括页面上存在或隐含的条目。

&#x200B;---

**6. 常见问题解答**

用户可能会询问关于此页面内容的3至6个问题，并提供简短答案。

```markdown
**FAQ:**
- **Q: [question]** — [short answer]
- **Q: [question]** — [short answer]
```

&#x200B;---

### 不应包含的内容

- 请&#x200B;**不要**&#x200B;重写或摘要页面的正文内容（该内容已经存在）。
- 请&#x200B;**不**&#x200B;包含分步说明（页面中的说明）。
- 请&#x200B;**不**&#x200B;创建该页面不支持的内容。

&#x200B;---

### 完整可折叠项模板

```markdown
+++AI Assistant — Page context

- **TL;DR:** [one sentence]

**Intents:**
- [intent]

**Glossary:**
- **[Term]**: [definition]

**Guardrails:**
- [guardrail]

**Terminology:**
- Canonical name: [name]
- Acronym: [acronym] — variants: [variants]

**FAQ:**
- **Q: [question]** — [short answer]

+++
```

&#x200B;---

## 注释

- 逐个处理文件，而不是批量处理文件，以保持较高的生成质量。
- 如果页面非常短或只是重定向/索引页面，请标记该页面，并询问用户是否要跳过它。
- 不创建新文件 — 仅编辑现有`.md`文件。
