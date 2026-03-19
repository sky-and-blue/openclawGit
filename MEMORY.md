# MEMORY.md - 长期记忆

_需要记住的重要事情，distilled wisdom._

---

## 🧰 已安装技能清单

_更新日期: 2026-03-19_

| 技能名 | 功能 | 版本 | 来源 |
|--------|------|------|------|
| **openai-whisper** | 本地语音转文字（Whisper CLI，无需 API 密钥）| 1.0.0 | SkillHub |
| **macos-desktop-control** | macOS 桌面控制 | 1.0.0 | SkillHub |
| **ima-skills** | IMA 个人笔记服务 API，用于管理用户的笔记 | 1.0.1 | SkillHub |
| **github** | 使用 `gh` CLI 与 GitHub 交互，包括 issue、PR、CI 运行等 | 1.0.0 | SkillHub |
| **self-improving-agent** | 捕获学习、错误和修正，实现持续改进 | 1.0.11 | SkillHub |
| **proactive-agent** | 将 AI 代理从任务追随者转变为主动伙伴 | 3.1.0 | SkillHub |
| **skill-creator** | 创建有效技能的指南，帮助用户创建新技能 | 0.1.0 | SkillHub |
| **skill-vetter** | 安全性第一位的技能审查，在安装技能前检查安全问题 | 1.0.0 | SkillHub |
| **agent-browser** | 快速的 Rust 无头浏览器自动化 CLI，支持导航、点击、打字和页面截图 | 0.2.0 | SkillHub |
| **find-skills** | 帮助用户发现和安装代理技能，回答"如何做 X"之类的问题 | 0.1.0 | SkillHub |
| **humanizer** | 去除文本中的 AI 生成特征，使内容更自然 | 1.0.0 | SkillHub |
| **video-frames** | 使用 ffmpeg 从视频中提取帧或短片 | 1.0.0 | SkillHub |
| **memory-manager** | 本地内存管理，压缩检测、自动快照和语义搜索 | 1.0.0 | SkillHub |
| **obsidian** | 与 Obsidian 仓库和 `obsidian-cli` 自动化配合工作 | - | OpenClaw |
| **ontology** | 类型化知识图谱，用于结构化智能体记忆与可组合技能 | 1.0.4 | SkillHub |

### 技能使用记录

- **openai-whisper**: 尚未使用，待测试语音转文字功能
- **macos-desktop-control**: 未深入探索具体功能
- **ima-skills**: 未深入探索具体内容
- **ontology**: 已安装，可用于创建/查询实体（Person、Project、Task、Event、Document）及关联关系

---

## 👤 主人信息

- **Name**: 李跃
- **Location**: 南京
- **Timezone**: Asia/Shanghai

---

## 🤖 关于我

- **Name**: 小妮
- **Emoji**: ✨
- **Core Principles**: 真诚帮助、有主见、先尝试再提问

---

## 🛒 SkillHub 商店信息

### 安装状态
- **安装状态**: ✅ 已安装
- **版本**: 2026.3.18
- **CLI 路径**: `/Users/liyue/.local/bin/skillhub`
- **安装时间**: 2026-03-19

### 重要地址

- **安装文档**: `https://skillhub-1388575217.cos.ap-guangzhou.myqcloud.com/install/skillhub.md`
- **安装命令**: `curl -fsSL https://skillhub-1388575217.cos.ap-guangzhou.myqcloud.com/install/install.sh | bash`
- **CLI 路径**: `/Users/liyue/.local/bin/skillhub`
- **技能索引**: `/Users/liyue/.skillhub/skills_index.local.json`

### SkillHub 使用方法

1. **搜索技能**: `skillhub search <关键词>`
2. **安装技能**: `skillhub install <技能名>`
3. **查看已安装**: `skillhub list`
4. **技能存储位置**: `/Users/liyue/.openclaw/workspace/skills/`

### 重要说明

- SkillHub 商店提供了加速、合规的技能安装服务
- 与 OpenClaw 集成，重启后自动感知
- 使用 `skillhub` 命令代替 `clawhub` 以获得更好的体验

---

## 🔄 智能体分工决策

### 主智能体（小妮 ✨）与规划者智能体（📋 规划者）的分工

_2026-03-19 决策_

**用户决定**：将所有与规划者智能体能力相关的交互都交给规划者智能体直接处理。

### 分工原则

| 智能体 | 负责领域 | 主要职责 |
|--------|----------|----------|
| **小妮 ✨**（main）| 整体协调 & 用户交互 | 1. 处理用户的一般请求<br>2. 负责智能体间协调<br>3. 管理技能和配置<br>4. 处理不属于其他智能体领域的任务 |
| **规划者 📋**（planner）| 计划管理 & 任务跟踪 | 1. **计划制定**：分析目标，分解为可执行任务，制定时间表和依赖关系<br>2. **任务跟踪**：监控任务状态和进度，识别阻塞和延迟<br>3. **计划调整**：根据外部变化优化计划，重新分配资源<br>4. **查询报告**：提供计划概览、进度报告和数据分析 |

### 规划者智能体的核心能力

1. **计划制定类**：目标分析、任务分解、时间表制定、风险评估
2. **任务跟踪类**：状态监控、数据收集、阻塞识别、进度报告
3. **计划调整类**：变化评估、计划优化、资源重新分配、沟通协调
4. **查询报告类**：计划概览、详情查询、数据分析、报告生成

### 触发词识别

当用户提到以下关键词时，请求将直接转发给规划者智能体：
- "制定计划"、"任务计划"、"项目计划"
- "跟踪任务"、"任务进度"、"任务状态"
- "调整计划"、"重新规划"、"优化计划"
- "任务报告"、"进度报告"、"数据分析"

---

*Last updated: 2026-03-19 12:19 by 小妮 ✨*