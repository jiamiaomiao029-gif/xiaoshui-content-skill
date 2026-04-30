# 小水同学的 Claude Code Skills 合集

包含三个核心 skill：
1. **xiaoshui-content** - 内容创作诊断
2. **dbs-xsz-chatroom** - 商业决策聊天室
3. **xiaoshui-update** - 一键自动更新

---

## 安装方法

### 方法一：一键安装（推荐）

```bash
cd ~/.claude/skills
git clone https://github.com/jiamiaomiao029-gif/xiaoshui-content-skill.git
cd ~/.claude/skills
ln -s xiaoshui-content-skill/xiaoshui-content xiaoshui-content
ln -s xiaoshui-content-skill/xiaoshui-update xiaoshui-update
ln -s xiaoshui-content-skill/dbs-xsz-chatroom dbs-xsz-chatroom
```

安装完成后，以后更新只需要在 Claude Code 中输入：

```
/xiaoshui-update
```

### 方法二：手动安装

1. 下载本仓库的所有文件
2. 将 `xiaoshui-content`、`xiaoshui-update` 和 `dbs-xsz-chatroom` 文件夹分别复制到 `~/.claude/skills/` 目录下

---

## 使用方式

安装后，在 Claude Code 中直接输入：

| Skill | 触发方式 |
|---|---|
| 内容创作诊断 | `/xiaoshui-content` |
| 商业决策聊天室 | `/dbs-xsz-chatroom` |
| 自动更新 | `/xiaoshui-update` |

或者直接描述你的问题，比如：
- "帮我做内容"、"不知道发什么"、"内容没人看"
- "我在纠结要不要..."、"帮我分析一下这个决策"

---

## 1. xiaoshui-content - 内容创作诊断

一个帮助自媒体创作者识别真需求、挖掘潜意识阻碍，用完整方法论陪伴式完成内容创作的 Claude Code skill。

### 适用场景

- 不知道做什么内容
- 有想法但不知道怎么做成好内容
- 做了内容但数据很差
- 有粉丝但不知道怎么变现
- 想建立完整的内容创作体系

### 功能特点

#### 1. 真需求诊断（挖掘真相）

不让你自欺欺人，直面真实需求：
- 识别**情绪问题 vs 事实问题**
- 挖掘**表面理由 vs 真正原因**
- 发现**人设冲突**（"高大上创作者" vs "搞转化变现"）
- 检验**产品-人群匹配**（粉丝为什么关注你 ≠ 他们会为什么买单）
- 区分**市场验证 vs 朋友反馈**（陌生人的钱才是真证据）

#### 2. 内容创作方法论（完整 SOP）

从 0 到 1 的全流程引导：

**Part 1: 准备自己**
- 提炼价值观（你相信什么、不信任什么）
- 找到最擅长的内容（脱下孔乙己的长衫）
- 建立语料库（flomo + 微信聊天记录提取）
- 用真实经历佐证观点

**Part 2: 准备热点**
- 基本功训练（拆解 30 个低粉爆款）
- 社会情绪捕捉（当前大众在焦虑什么）
- 爆款规律积累（形成自己的文档）

**Part 3: 具体操作**
- 选题三来源（自己感受/热点话题/社会情绪）
- AI 辅助创作流程（语料库 + 热点观点 → 初稿 → 去 AI 味）
- 封面标题生成

**Part 4: 内容类型设计**
- **流量内容**：情绪走在内容前面，让用户转发
- **粉丝内容**：内容走在情绪前面，让用户进主页
- **变现内容**：制造焦虑 + 留悬念，让用户找咨询

每条内容发布前的三问：
1. 这条内容的类型是什么？
2. 用户看完后的下一个动作是什么？
3. 我能预测到用户的反应吗？

#### 3. 实践论闭环（持续迭代）

认识 → 实践 → 新认识 → 新实践（螺旋上升）：
- AB 测试心态（允许出错、优化单点）
- 对失败的好奇（不是理性看待，而是天生好奇）
- 粗茶淡饭、平静推进（只盯具体细节，不幻想结果）
- 复利效应建立（固定时间、形成 SOP）

### 方法论来源

基于真实创作者的 549 条实战笔记，融合：
- 商业诊断思维（产品-人群匹配、真需求识别）
- 毛选思维（矛盾论 + 实践论）
- don 哥思维（对失败的好奇、情绪问题 vs 事实问题）
- 谢胜子思维（粗茶淡饭、平静推进、复利效应）

---

## 2. dbs-xsz-chatroom - 商业决策聊天室

让谢胜子和 don 哥同时分析你的商业决策问题，互相指出逻辑谬误，帮你看清盲区。

### 适用场景

- 面临重要商业决策，不确定该怎么选
- 想要多角度审视自己的想法
- 需要有人指出思维盲区和逻辑漏洞
- 想听听"长期主义"和"快速试错"两种思维的碰撞

### 功能特点

**第一轮：各自分析**
- 谢胜子：从长期主义、粗茶淡饭、平静推进的角度分析
- don 哥：从快速试错、对失败的好奇、行动偏好的角度分析

**第二轮：互相质疑**
- 谢胜子指出 don 哥可能过于冒进的地方
- don 哥指出谢胜子可能过于保守的地方

**判官总结**
- Claude 总结两种思维的核心分歧
- 指出互补点和冲突点
- 给出可执行的综合建议

---

## 3. xiaoshui-update - 自动更新工具

一键从 GitHub 拉取最新版本，自动安装/更新所有 skills。

- 自动检测本地是否已安装
- 从 GitHub 拉取最新版本
- 自动创建软链接到 skills 目录
- 显示更新日志和变更内容

---

## 文件结构

```
xiaoshui-content-skill/
├── xiaoshui-content/
│   ├── skill.md          # Skill 说明文档
│   ├── agent.md          # Agent 行为指令
│   └── knowledge.md      # 核心方法论知识库
├── xiaoshui-update/
│   ├── skill.md          # Skill 说明文档
│   └── agent.md          # Agent 行为指令
├── dbs-xsz-chatroom/
│   ├── skill.md          # Skill 说明文档
│   └── agent.md          # Agent 行为指令
├── README.md             # 本文件
└── LICENSE               # MIT 许可证
```

## 与其他 skill 的配合

- 先用 `dbs-diagnosis` 诊断商业模式（战略层面）
- 用 `dbs-xsz-chatroom` 做商业决策（决策层面）
- 再用 `xiaoshui-content` 落地到具体内容创作（执行层面）

## 作者

[@jiamiaomiao029-gif](https://github.com/jiamiaomiao029-gif)

---

**如果这个 skill 对你有帮助，欢迎 Star ⭐️**
