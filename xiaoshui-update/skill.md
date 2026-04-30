---
name: xiaoshui-update
description: 自动更新小水同学的 skills 到最新版本。从 GitHub 拉取最新代码并安装到本地。触发方式：/xiaoshui-update、/更新小水skills、「更新小水技能」
---

# xiaoshui-update：自动更新小水 Skills

自动从 GitHub 拉取小水同学的最新 skills 并安装到本地。

---

## 功能

- 自动检测本地是否已安装
- 从 GitHub 拉取最新版本
- 自动安装/更新到 `~/.claude/skills/` 目录
- 显示更新日志

---

## 使用方式

```
/xiaoshui-update
/更新小水skills
```

或者直接说：
- "更新小水的技能"
- "拉取最新版本"
- "更新 xiaoshui skills"

---

## 更新的 Skills

- **xiaoshui-content** - 内容创作诊断
- **dbs-xsz-chatroom** - 商业决策聊天室

---

## 工作流程

1. 检测本地是否已有仓库
2. 如果有：`git pull` 拉取最新版本
3. 如果没有：`git clone` 克隆仓库
4. 创建/更新软链接到 skills 目录
5. 显示更新内容
