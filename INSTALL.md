---
source-git-commit: 08eaa7ae974c134ea2e920a1fa854dcf6a971e18
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

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

3. 代理程序将自动：
   - 测试SSH和HTTPS访问
   - 使用工作方法
   - 指导您完成设置（如果需要）
4. 完成！✨

**注意：**&#x200B;代理自动检测您是否对`git.corp.adobe.com`具有SSH或HTTPS访问权限，并使用适当的方法。 如果这两种方法都不起作用，则会提供引导式设置。

### 选项2：使用终端

1. 在存储库根目录中打开终端
2. 运行：

   ```bash
   ./setup-agents.sh
   ```

   脚本将自动：
   - 测试SSH和HTTPS访问
   - 使用工作方法
   - 显示设置说明（如果需要）

   或手动（如果您知道Git已配置）：

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

有关可用代理的完整列表，请参阅[AGENTS.md](AGENTS.md)。

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
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

子模块指向：
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

这可确保每个人都使用相同的、最新的代理。

## 对于维护者

### 添加到新存储库

1. 添加子模块：

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. 复制安装文件：
   - `setup-agents.sh`
   - `setup-agent.md` （放在根中，而不是子模块中）
   - `INSTALL.md`

3. 提交：

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### 更新中央存储库

应在以下位置对代理进行更改：
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

所有存储库都将通过`git submodule update --remote`接收更新。

&#x200B;---

**需要帮助？**&#x200B;请与文档团队负责人联系或查看内部Wiki。
