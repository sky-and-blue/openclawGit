## [LRN-20260319-001] best_practice
**Logged**: 2026-03-19T06:46:00+08:00
**Priority**: medium
**Status**: pending
**Area**: config

### Summary
记录proactive-agent技能的核心功能和使用方法

### Details
proactive-agent是主动式AI助手技能，核心能力包括：
1. 自动持久化用户输入的重要信息（偏好、决定、参数等），避免会话重启丢失上下文
2. 主动预判用户需求，自动跟进待办任务、定时提醒
3. 遇到问题自动尝试最多10种解法，减少用户负担
4. 自动安全审核：安装新技能、访问外部内容前自动做风险检查
5. 自动优化：每周整理交互记录，将重复流程自动化

用户可主动触发的指令：
- "查看当前主动任务"：列出所有自动跟进的待办、定时任务
- "调整主动提醒频率"：自定义提醒时间/频率或关闭非紧急提醒
- "帮我优化当前工作流"：分析操作给出自动化建议
- "安全检查"：扫描所有技能、配置的安全风险

### Suggested Action
后续用户提到主动提醒、自动化需求时，优先使用proactive-agent的能力实现

### Metadata
- Source: user_feedback
- Related Files: /Users/liyue/.openclaw/workspace/skills/proactive-agent/SKILL.md
- Tags: proactive, skill-usage

---
## [LRN-20260319-002] best_practice
**Logged**: 2026-03-19T06:47:00+08:00
**Priority**: medium
**Status**: pending
**Area**: config

### Summary
记录skill-creator技能的核心功能和使用方法

### Details
skill-creator是自定义技能创建/优化工具，核心能力：
1. 自动生成符合SkillHub规范的技能模板，支持目录结构、SKILL.md、示例脚本
2. 自动校验技能规范性、安全风险，避免冗余内容和无效引用
3. 支持现有技能优化，减少token占用优化
4. 支持一键打包发布到SkillHub商店

触发场景（自动识别用户指令）：
- 用户提到"创建/优化/发布技能"、"把流程做成技能"、"审核技能"等内容
- 用户需要自定义可复用的专业领域操作流程
- 优化现有技能的性能/安全性

用户指令：
- "帮我创建一个XX技能，功能是XXX" → 自动生成完整技能模板
- "优化这个技能" → 自动分析问题并更新
- "把这个技能发布到商店" → 自动校验打包后发布到SkillHub
- "检查这个技能有没有安全问题" → 自动扫描脚本和外部调用风险

### Suggested Action
后续用户提到技能创建/优化/发布需求时，优先使用skill-creator实现

### Metadata
- Source: user_feedback
- Related Files: /Users/liyue/.openclaw/workspace/skills/skill-creator/SKILL.md
- Tags: skill-creator, skill-development

---
