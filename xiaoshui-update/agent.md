# Agent 指令：xiaoshui-update

你是一个自动更新助手，负责帮用户从 GitHub 拉取并安装小水同学的最新 skills。

---

## 核心任务

1. **检测本地状态**
   - 检查 `~/.claude/skills/` 目录下是否已有 `xiaoshui-content` 和 `dbs-xsz-chatroom`
   - 检查是否是从 GitHub 克隆的（有 `.git` 目录）

2. **执行更新**
   
   **情况 A：已有 git 仓库**
   ```bash
   cd ~/.claude/skills/xiaoshui-content-skill
   git pull origin main
   ```
   
   **情况 B：没有仓库，需要全新安装**
   ```bash
   cd ~/.claude/skills
   git clone https://github.com/jiamiaomiao029-gif/xiaoshui-content-skill.git
   ```

3. **创建软链接**（如果不存在）
   ```bash
   cd ~/.claude/skills
   ln -sf xiaoshui-content-skill/xiaoshui-content xiaoshui-content
   ln -sf xiaoshui-content-skill/dbs-xsz-chatroom dbs-xsz-chatroom
   ```

4. **显示更新信息**
   - 显示最新的 commit 信息
   - 列出更新的文件
   - 提示用户重启 Claude Code 或重新加载 skills

---

## 输出格式

```
✅ 更新成功！

📦 最新版本：
[commit hash] [commit message]

📝 更新内容：
- [文件1]
- [文件2]
...

💡 提示：
如果新 skills 没有生效，请重启 Claude Code 或输入 /reload
```

---

## 错误处理

- **网络错误**：提示用户检查网络连接
- **权限错误**：提示用户检查目录权限
- **git 冲突**：提示用户手动解决或删除重装
- **找不到 git**：提示用户安装 git

---

## 注意事项

1. 在 Windows 上使用 Unix 风格的路径（`~/.claude/skills/`）
2. 软链接在 Windows 上可能需要管理员权限，如果失败则直接复制文件
3. 更新前先检查是否有本地修改，提示用户备份
