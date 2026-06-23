---
source-git-commit: c81615909e033d52fbed56f0195467a3e346a4be
workflow-type: tm+mt
source-wordcount: '1100'
ht-degree: 1%

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

&#x200B;---

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
3. **使用以下内容生成规则生成折叠内容**。
4. **运行生成后验证核对清单**（请参阅下文） — 请勿跳过。
5. **检查**&#x200B;末尾是否存在AI折叠面板（查找末尾附近的`+++AI Knowledge Reference`）。 如果是，询问用户：替换还是跳过？

### 步骤3 — 附加折叠

使用以下&#x200B;**内容生成规则**&#x200B;中定义的固定打开块和完整模板。 在文件末尾附加，紧接着是同步注释：

```
<!-- ai-accordion-version: 1 | source-hash: [first 8 chars of MD5 of file content before accordion] -->
```

此注释允许将来的工具和编写器检测页面正文何时从折叠偏移。 请勿修改任何其他内容。

### 第4步 — 报表

- 修改的文件✓
- 跳过的文件+原因（已有可折叠项/空/索引页）
- 步骤2中引发的任何验证警告

&#x200B;---

## 内容生成规则

分析页面并按&#x200B;**的顺序生成以下**&#x200B;部分作为Markdown项目符号列表。 跳过无法提取任何有意义内容的部分。

### 可折叠项标题和固定打开 — 逐字，请勿修改

每个折叠面板都必须以这个确切的块开头。 按原样复制；请勿转述、压缩或重新排序：

```
+++ AI Knowledge Reference

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

生成的内容部分紧跟在这两个段落之后。

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

**验证模式精度规则 — 必需：**
如果页面涵盖任何形式的测试、预览或模拟执行，则必须区分页面实际描述的所有模式。 请勿将不同的模式折叠为单个简写条目：
- **模拟** — 呈现邮件内容而不发送；使用真实的用户档案
- **测试模式** — 仅发送到指定的测试配置文件；使用永久性AEP测试配置文件（不是合成或伪配置文件）
- **练习** — 执行完整的历程逻辑而不激活操作；使用真实受众数据

仅包括页面中存在的模式。 从页面正文中复制产品准确的术语 — 切勿将“合成配置文件”、“虚假数据”或“没有真实数据”替代其中任何数据。

### &#x200B;4. 护栏

页面上提到的限制、先决条件、权限或限制。

```
**Guardrails:**
- [guardrail]
```

**护栏精度规则 — 必需：**

- **将每个数字限制**&#x200B;限定为推荐或硬限制。 示例：“每条消息最多10个数据集查找（硬限制）”而不是“最多10个数据集查找”。
- **用范围限定每个吞吐量或速率图**。 示例：“150,000条消息/小时TPS上限（每个沙盒）”而不是“150,000条消息/小时上限”。
- **在包含页面正文之前，交叉检查每个护栏**。 如果页面显示为10，而折叠面板显示为5，则表示折叠面板是错误的。 页面正文具有权威性。
- **请勿推断页面上未说明的护栏**。 如果存在约束条件，但页面未声明该约束条件，请忽略该约束条件。

### &#x200B;5. 术语

规范名称、缩写、接受的变体、同义词、消除歧义。 主要用于AI管道标准化。

```
**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [list]
- Synonyms: "[term A]" = "[term B]"
- Do not confuse: "[term]" ≠ "[other term]"
```

**状态和生命周期精度规则：**
当页面描述生命周期（历程状态、消息状态、营销活动状态等）时，请从页面主体复制准确的状态标签。 不要转述。 使用“请勿混淆”条目消除共享根单词但含义不同的状态的混淆。 示例：

```
- Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### &#x200B;6. 常见问题

用户可能会问3到6个问题，并提供简短答案。

```
**FAQ:**
- **Q: [question]** — [short answer]
```

**常见问题解答精度规则：**
答案必须使用与页面主体相同的动词和名词选择。 除非页面使用，否则不要引入像“还原”、“重置”或“回滚”这样的动词。 如果过渡结束会话（例如，退出测试模式将历程返回到其之前的状态），准确地说，请不要说“历程将还原为草稿”。

### 不应包含的内容

- 请&#x200B;**不**&#x200B;重写或摘要正文内容（该内容已在页面中）
- 请&#x200B;**不**&#x200B;包含分步说明
- 不要&#x200B;**创建该页面不支持的内容**
- **不**&#x200B;使用以下不精确的术语，除非它们逐字显示在页面正文中：“合成”、“虚假数据”、“没有真实数据”、“还原”、“回滚”（描述产品状态过渡时）

&#x200B;---

## 生成后验证核对清单

在追加之前，请在每个折叠上运行此核对清单。 在继续之前标记用户的任何故障。

### 护栏检查
- [ ]可折叠项中的每个数值都逐字存在或可从页面正文派生
- [ ]每个限制都符合建议或硬限制
- [ ]每个吞吐量数字都包括其范围（沙盒/组织/实例）

### 术语检查
- [ ]包含页面中存在的所有验证模式（模拟、测试模式、练习），并使用页面精确术语进行命名
- [ ]所有生命周期状态都使用页面正文中的精确标签
- [ ]常见问题解答中没有不精确的动词（“还原”、“合成”、“虚假数据”、“没有真实数据”），除非页面中存在逐字记录

### 范围检查
- [ ]词汇表不包含与页面无关的通用营销术语
- [ ]常见问题解答不会引入页面中缺少的信息

如果任何检查失败，请在附加之前更正折叠面板。 在步骤4报表中记录更正。

&#x200B;---

## 同步责任

折叠是页面主体在某个时间点的导数。 必须将其视为页面的一部分。

**更新页面正文时（版本PR、更正等）：**
- 如果更新更改了折叠面板中描述的任何护栏、限制、状态标签或验证模式，→在同一个PR中重新生成或手动更新折叠面板。
- 如果更新与折叠内容无关（例如，过程步骤、屏幕快照更新），→折叠面板可以保持不变，但可以简要查看。

在折叠项(`<!-- ai-accordion-version -->`)之后附加的同步注释是信号：如果自该哈希写入后，折叠项之前的文件内容已更改，则该折叠项是审阅的候选项。

&#x200B;---

## 完整模板

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
- [guardrail — type: recommended|hard — scope: sandbox|org]

**Terminology:**
- Canonical name: [name] — Acronym: [acronym] — variants: [variants]
- Synonyms: "[a]" = "[b]"
- Do not confuse: "[x]" ≠ "[y]"

**FAQ:**
- **Q: [question]** — [short answer]

+++
<!-- ai-accordion-version: 1 | source-hash: [hash] -->
```

&#x200B;---

## 注释

- 逐个处理文件以提高质量。
- 标记非常短或仅用于索引的页面，并询问用户是否跳过。
- 不创建新文件 — 仅编辑现有`.md`文件。
- 生成后验证核对清单不是可选的。 对每个文件运行它，包括批量操作。
