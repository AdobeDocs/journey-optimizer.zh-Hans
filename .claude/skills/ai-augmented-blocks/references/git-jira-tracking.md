---
source-git-commit: 469248d3ded81c5e3aaa9a2ccf04c0ca0c22a5d0
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 2%

---
# Git、PR和JIRA跟踪

如何安全着陆并跟踪更改。 作者提出两个确定的规则：

1. 打开PR前&#x200B;**询问。** 无论如何生成并验证块，但仅打开拉取
如果作者答应，则请求。
2. **从不合并。** 这些公关(PR)是供人审查的。 合并始终由作者决定。

## 结构扫描（提交前运行）

对于文件夹中处理的每个页面：

```bash
cd <repo>
for p in <page1> <page2> ...; do
  f="help/_includes/do-not-localize/<folder>/ai-augmented-$p.md"
  inc="help/using/<folder>/$p.md"
  [ -f "$f" ] || echo "MISSING BLOCK: $f"
  grep -q '^# AI Knowledge Reference' "$f"            || echo "$p: missing H1"
  grep -q '^+++ AI Knowledge Reference' "$f"          || echo "$p: missing accordion open"
  grep -q 'This section contains structured knowledge' "$f" || echo "$p: missing opening para 1"
  grep -q 'ai-section-version' "$f"                   || echo "$p: missing sync comment"
  grep -nEi "\b(isn't|aren't|don't|doesn't|didn't|can't|won't|wouldn't|couldn't|shouldn't|it's|we've|we're|you're|they're|that's|there's|haven't|hasn't|wasn't|weren't)\b" "$f" \
    | grep -vi 'UICONTROL' && echo "  ^ $p contraction"
  grep -q "do-not-localize/<folder>/ai-augmented-$p.md" "$inc" || echo "$p: MISSING include in page"
done
echo "=== sweep done ==="
git status --short
```

任何打印的行（“扫描完成”和`git status`列表除外）都是以前要修复的缺陷
提交。

## 分支并提交（从不提交主）

```bash
git checkout main -q && git pull -q origin main
git checkout -q -b DOCAC-<key> origin/main    # branch name = the JIRA task key
# ... generate + verify + sweep ...
git add help/_includes/do-not-localize/<folder>/ help/using/<folder>/*.md
git commit -q -m "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)

<one-line what + the verification result>

Co-Authored-By: Claude <model> <noreply@anthropic.com>"
```

**验证承诺是否落在分支上，而不是在`main`**(已知的步枪，如果您切换到
`main`要检查页面，稍后提交可能会登陆该页面)：

```bash
git rev-parse --abbrev-ref HEAD                    # must print DOCAC-<key>
git rev-list --left-right --count origin/main...DOCAC-<key>   # must show  0<TAB>1
```

如果承诺意外抵达`main`： `git branch -f DOCAC-<key> <sha>`以指向分支
在该处，`git checkout DOCAC-<key>`，然后`git branch -f main origin/main`重置本地主节点。
`origin/main`绝不受本地错误的影响。

推送： `git push -u origin DOCAC-<key>` (如果该分支已存在，则使用`--force-with-lease`
远程提交)。

## 询问PR

简单询问作者，例如： *&quot;已为`<folder>`生成并验证块。 您是否希望
要打开PR进行审阅吗？“*” 仅当满足以下条件时：

```bash
gh pr create --base main --head DOCAC-<key> \
  --title "DOCAC-<key> Add AI Knowledge Reference blocks (<folder>)" \
  --body-file <pr-body>.md
```

PR正文以所需的归因行结尾
(`🤖 Generated with [Claude Code](https://claude.com/claude-code)`). **不合并** — 保留
PR开放供审查。

## JIRA跟踪

跟踪DOCAC任务中的每个更改（转出史诗：`DOCAC-15582`）。 查找或创建文件夹的
任务，然后：

1. **带有更改内容和验证结果（已覆盖/跳过的页面，验证程序）的注释**
清理/更正了，任何值得注意的硬调用与默认调用)。 包括PR链接（如果已打开）。
2. **设置修复版本** （此程序使用了`AJO26.9`）。
3. 根据您的工作流，**过渡**正在处理→已解决的新区→（分辨率“已修复”）。 在此
项目过渡ID为`4`（开始进度），然后`5`（解决，含分辨率）
   `{"name":"Fixed"}`)；必须先启动仍处于“新”状态的任务，然后才能解决该任务。

使用公司JIRA MCP工具(`fixVersions`的`add_jira_comment`，`update_jira_issue`，
`bulk_transition_jira_issues`)或JIRA UI。 如果您没有JIRA访问权限，请将此步骤移至
有人拥有它，并在您的报告中记录它。

## 一个文件夹=一个分支=一个任务

请勿在单个分支或PR中混合使用不相关的文件夹。 稍后添加的新页面本身很小
更改（“创建”模式），并且可以根据您的团队偏好共享文件夹的任务或获取自己的任务。
