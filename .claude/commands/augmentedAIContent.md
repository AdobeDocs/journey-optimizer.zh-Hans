---
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: '1406'
ht-degree: 0%

---
# augmentedAIContent

在Journey Optimizer文档存储库中的一个或多个Markdown文件的末尾附加自动生成的&#x200B;**快速引用**&#x200B;部分。

## 目标存储库

`help/using/` （相对于存储库根）

## 部分和选项卡语法(Experience League)

### 区域标题

```
## Quick reference {#quick-reference}
```

### 选项卡

```
>[!BEGINTABS]

>[!TAB Tab name]

Content here — any standard markdown is valid.

>[!TAB Another tab]

Content here.

>[!ENDTABS]
```

**规则：**

- `>[!BEGINTABS]`和`>[!ENDTABS]`各自占一行，由空白行括起来
- `>[!TAB Name]`位于其自身的行中，内容前跟有一行空白
- 选项卡名称为标题大小写、简短（1-3字）
- `>[!BEGINTABS]`之前和`>[!ENDTABS]`之后的空白行

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
3. **使用以下内容生成规则生成节内容**。
4. **运行生成后验证核对清单**（请参阅下文） — 请勿跳过。
5. **检查**&#x200B;是否快速引用部分已存在于末尾（查找末尾附近的`## Quick reference`）。 如果是，询问用户：替换还是跳过？

### 步骤3 — 验证针对页面正文的每个声明

在追加之前，请通过声明重新读取生成的部分声明。 此步骤是&#x200B;**强制性的，不能跳过**，即使对于短文件也是如此。 在继续执行步骤4之前，请更正所有故障。

**术语和标签**

- [ ]部分中的每个术语、标签和UI名称都会显示在页面正文中 — 不是从其他页面导入的，也不是从一般产品知识推断的
- [ ]未列出同义词，除非页面上同时出现两个表单
- [ ]每个“请勿混淆”条目仅引用此页面上提到的概念

**护栏和限制**

- [ ]每个数值都与页面正文完全匹配
- [ ]仅当页面正文使用该词或明确暗示系统强制使用该词时，限制才称为&#x200B;**hard**（例如，“不能超过”、“允许的最大值……”、“仅……支持”）
- [ ]仅当页面正文使用该词或等效词时，才将限制称为&#x200B;**推荐**（“为获得最佳性能”，“推荐”）
- [ ]如果页面正文未提供限定符，则部分将不提供 — 不创建限定符
- [ ]没有关于源页面是否陈述的元注释（例如，“此页面上未说明任何具体数字”）

**词汇表定义**

- [ ]页面正文中没有定义包含技术详细信息
- [ ]使用文档集中其他页面的信息没有条目详述

**常见问题解答**

- [ ]每个特定详细信息（UI提供、按钮名称、字段名称、步骤序列）都记录在页面正文中 — 未从其他页面推断或导入
- [ ]没有答案引入页面正文未寻址的信息

**更正规则：**&#x200B;如果任何检查失败，则在&#x200B;**之前更正内容**。 在步骤5报表中记录每次校正。

---

### 步骤4 — 附加部分

使用以下&#x200B;**内容生成规则**&#x200B;中定义的固定打开块和完整模板。 在文件末尾附加，紧接着是同步注释：

```
<!-- ai-section-version: 1 | source-hash: [first 8 chars of MD5 of file content before section] -->
```

此注释允许将来的工具和编写器检测页面正文何时从部分偏移。 请勿修改任何其他内容。

### 步骤5 — 报表

- 修改的文件✓
- 跳过的文件+原因（已有部分/空/索引页）
- 步骤2中引发的任何验证警告

---

## 内容生成规则

分析该页面并按&#x200B;**的顺序生成低于**&#x200B;的选项卡。 如果无法提取任何有意义的内容，则完全跳过选项卡。

### 节标题和固定开口 — 逐字，请勿修改

每个快速引用部分都必须以这个确切的块开头。 按原样复制；请勿转述、压缩或重新排序：

```
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.
```

`>[!BEGINTABS]`块紧跟在这两个段落之后。

### 选项卡1 — 概述

一句的TL；DR摘要，该页面教导或支持的内容，随后是用户在阅读本页面后可以完成的3-6件事。

```
>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [action]
* [action]
```

### 选项卡2 — 术语表

此页面/功能的特定关键术语，带有简短定义。 标记特定于产品的术语。

```
>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*
```

仅包含与此页面相关的术语。 不要使用通用的营销词语进行填充。

**验证模式精度规则 — 必需：**
如果页面涵盖任何形式的测试、预览或模拟执行，则必须区分页面实际描述的所有模式。 请勿将不同的模式折叠为单个简写条目：
- **模拟** — 呈现邮件内容而不发送；使用真实的用户档案
- **测试模式** — 仅发送到指定的测试配置文件；使用永久性AEP测试配置文件（不是合成或伪配置文件）
- **练习** — 执行完整的历程逻辑而不激活操作；使用真实受众数据

仅包括页面中存在的模式。 从页面正文中复制产品准确的术语 — 切勿将“合成配置文件”、“虚假数据”或“没有真实数据”替代其中任何数据。

### 选项卡3 — 术语

规范名称、缩写、接受的变体、同义词、消除歧义。 主要用于AI管道标准化。

```
>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [list]
* **Synonyms:** "[term A]" = "[term B]"
* **Do not confuse:** "[term]" ≠ "[other term]"
```

**状态和生命周期精度规则：**
当页面描述生命周期（历程状态、消息状态、营销活动状态等）时，请从页面主体复制准确的状态标签。 不要转述。 使用“请勿混淆”条目消除共享根单词但含义不同的状态的混淆。 示例：

```
* Do not confuse: "Stop" (user-initiated action) ≠ "Stopped" (resulting status) ≠ "Close" (action on Live journey allowing in-progress profiles to finish) ≠ "Closed" (resulting status)
```

### 选项卡4 — 护栏和限制

页面上提到的限制、先决条件、权限或限制。

```
>[!TAB Guardrails & Limitations]

* [guardrail]
```

**护栏精度规则 — 必需：**

- **将每个数字限制**&#x200B;限定为推荐或硬限制。 示例：“每条消息最多10个数据集查找（硬限制）”而不是“最多10个数据集查找”。
- **用范围限定每个吞吐量或速率图**。 示例：“150,000条消息/小时TPS上限（每个沙盒）”而不是“150,000条消息/小时上限”。
- **在包含页面正文之前，交叉检查每个护栏**。 如果页面显示10，而部分显示5，则部分错误。 页面正文具有权威性。
- **请勿推断页面上未说明的护栏**。 如果存在约束条件，但页面未声明该约束条件，请忽略该约束条件。

### 选项卡5 — 常见问题解答

用户可能会问3到6个问题，并提供简短答案。 将每个问题格式化为粗体问题标题，后跟段落答案。

```
>[!TAB FAQ]

**Q: [question]**

[short answer]
```

**常见问题解答精度规则：**
答案必须使用与页面主体相同的动词和名词选择。 除非页面使用，否则不要引入像“还原”、“重置”或“回滚”这样的动词。 如果过渡结束会话（例如，退出测试模式将历程返回到其之前的状态），准确地说，请不要说“历程将还原为草稿”。

### 不应包含的内容

- 请&#x200B;**不**&#x200B;重写或摘要正文内容（该内容已在页面中）
- 请&#x200B;**不**&#x200B;包含分步说明
- 不要&#x200B;**创建该页面不支持的内容**
- **不**&#x200B;使用以下不精确的术语，除非它们逐字显示在页面正文中：“合成”、“虚假数据”、“没有真实数据”、“还原”、“回滚”（描述产品状态过渡时）

---

## 生成后验证核对清单

在追加之前，请在每个部分运行此核对清单。 在继续之前标记用户的任何故障。

### 护栏检查

- [ ]节中的每个数值都逐字存在或可从页面正文派生
- [ ]每个限制都符合建议或硬限制
- [ ]每个吞吐量数字都包括其范围（沙盒/组织/实例）

### 术语检查
- [ ]包含页面中存在的所有验证模式（模拟、测试模式、练习），并使用页面精确术语进行命名
- [ ]所有生命周期状态都使用页面正文中的精确标签
- [ ]常见问题解答中没有不精确的动词（“还原”、“合成”、“虚假数据”、“没有真实数据”），除非页面中存在逐字记录

### 范围检查
- [ ]词汇表不包含与页面无关的通用营销术语
- [ ]常见问题解答不会引入页面中缺少的信息

如果任何检查失败，请先更正部分，然后再进行附加。 在步骤4报表中记录更正。

---

## 同步责任

快速引用部分是指页面主体在某个时间点的派生。 必须将其视为页面的一部分。

**更新页面正文时（版本PR、更正等）：**

- 如果更新更改了部分中描述的任何护栏、限制、状态标签或验证模式，→在同一PR中重新生成或手动更新部分。
- 如果更新与部分内容无关（例如过程步骤、屏幕快照更新），→部分可以保持不变，但可简短查看。

在节(`<!-- ai-section-version -->`)之后附加的同步注释是信号：如果自写入该哈希后，节之前的文件内容已更改，则该节是候选审阅。

---

## 完整模板

```markdown
## Quick reference {#quick-reference}

This section contains structured knowledge intended to support interpretation, retrieval, and question answering related to this topic.

For complete understanding, this information should be combined with the documentation on this page. Neither source is intended to stand alone; the page describes the feature, while this section provides additional context that helps disambiguate terminology, intent, applicability, and constraints.

>[!BEGINTABS]

>[!TAB Overview]

**TL;DR**

[one sentence]

**Intents**

* [intent]

>[!TAB Glossary]

* **[Term]**: [definition] *(product-specific)*

>[!TAB Terminology]

* **Canonical name:** [name] — Acronym: [acronym] — variants: [variants]
* **Synonyms:** "[a]" = "[b]"
* **Do not confuse:** "[x]" ≠ "[y]"

>[!TAB Guardrails & Limitations]

* [guardrail — type: recommended|hard — scope: sandbox|org]

>[!TAB FAQ]

**Q: [question]**

[short answer]

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: [hash] -->
```

## 注释

- 逐个处理文件以提高质量。
- 标记非常短或仅用于索引的页面，并询问用户是否跳过。
- 不创建新文件 — 仅编辑现有`.md`文件。
- 生成后验证核对清单不是可选的。 对每个文件运行它，包括批量操作。
