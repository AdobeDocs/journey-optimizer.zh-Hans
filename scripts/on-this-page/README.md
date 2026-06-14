---
source-git-commit: a4123db7ae90552a15e6f425bce0037426053a78
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 0%

---
# “在此页面上”框工具

用于添加和验证标准&#x200B;**“在此页面上”**&#x200B;顶部阴影框的工具
AJO文档页面。查看`.cursor/rules/on-this-page-box.mdc`中的规范。
在epic **DOCAC-14936**&#x200B;下跟踪转出（每个顶级文件夹一个任务）。

## 箱子是什么样的

```text
# Page Title {#anchor}

>[!BEGINSHADEBOX]

**On this page:** <one clear sentence describing the page's purpose>

>[!ENDSHADEBOX]
```

## 建议的工作流（每个文件夹/Jira任务）

从存储库根目录(`journey-optimizer.en/`)运行。

1. **插入框** (从每个页面的正文植入第一稿句子
   `description`). 机械的、幂等的、永远不会触及前题：

   ```bash
   python scripts/on-this-page/add_on_this_page.py help/using/reports --seed-from-description
   ```

   使用`--dry-run`先预览。

2. **优化措辞。** 种子是一个起点 — 编辑每个句子
读为目的陈述（一句话、纯文本、美式英语）。 如果您
跳过`--seed-from-description`，改为插入`{{TODO...}}`占位符，并且
该验证器将标记任何剩余部分。

3. 打开PR前&#x200B;**验证**：

   ```bash
   python scripts/on-this-page/validate_on_this_page.py help/using/reports --require
   ```

   退出代码在任何失败时都是非零的，因此它可以引导CI。

## 范围/排除项

默认情况下排除引用页面和语法页面(路径部分`api-reference`，
`expression`, `functions`). 如果需要，使用`--exclude ...`进行覆盖。

## 存储库范围的进度检查

```bash
python scripts/on-this-page/validate_on_this_page.py help
```

如果没有`--require`，仍缺少框的页面将被报告为`pending`(而不是
失败)，以便您可以在指南中跟踪转出进度。
