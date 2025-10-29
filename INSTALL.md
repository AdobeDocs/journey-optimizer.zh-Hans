---
source-git-commit: d7bb3424bc6dfb837b47d15c448a2d46bf4b6c3c
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---
# 🚀正在安装游标代理

光标代理是帮助您更高效地创建和维护文档的共享工具。

## 首次设置

您只需为每个存储库执行&#x200B;**次**。

### 选项1：使用游标（建议的⭐）

1. 打开光标聊天（`Cmd+L`或`Ctrl+L`）
2. 类型：

   ```
   @setup-agents
   ```

3. 按照提示操作
4. 完成！✨

### 选项2：使用终端

1. 在存储库根目录中打开终端
2. 运行：

   ```bash
   ./setup-agents.sh
   ```

   或手动：

   ```bash
   git submodule update --init --recursive
   ```

3. 完成！✨

## 验证

安装后，验证安装：

```bash
ls .cursor-agents/agents/
```

您应会看到：
- `draft-page-generator.md`
- `fix-grammar.md`
- 以此类推。

## 使用情况

安装之后，您可以在光标中使用代理：

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

有关可用代理的完整列表，请参阅`.cursor-agents/AGENTS.md`。

## 更新代理

要获取所有代理的最新版本，请执行以下操作：

### 选项1：使用光标

```
@update-agents
```

### 选项2：使用终端

```bash
git submodule update --remote
```

## 故障排除

### “未找到代理”错误

如果看到此错误，则表示尚未安装代理。 运行：

```
@setup-agents
```

### 子模块为空

如果`.cursor-agents/`存在但为空：

```bash
git submodule update --init --recursive --remote
```

### 拒绝权限

确保安装脚本可执行：

```bash
chmod +x setup-agents.sh
```

### 网络/VPN问题

- 确保已连接到Adobe VPN
- 检查网络连接
- 验证Git访问权限：

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## 工作原理

游标代理作为&#x200B;**Git子模块**&#x200B;分发：

```
journey-optimizer.en/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  ├── setup-agent.md           ← Bootstrap agent
  └── help/                    ← Your documentation
```

子模块指向：
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

这可确保每个人都使用相同的、最新的代理。

&#x200B;---

**需要帮助？**&#x200B;请与文档团队负责人联系或查看内部Wiki。

