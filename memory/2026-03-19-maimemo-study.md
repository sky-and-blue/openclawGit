# Session: 2026-03-19 06:48:11 UTC

- **Session Key**: agent:main:feishu:direct:ou_7f5c8f2774475eabd071360f959caf5e
- **Session ID**: 9dd338f8-f579-4970-8b30-dd0cbf93222c
- **Source**: feishu

## Conversation Summary

assistant: ✅ 接口调用成功！共获取到今日206个学习单词：
---
### 📊 学习情况汇总
- ✅ 已完成：6个
- ⏳ 未完成：200个
- 🆕 今日新学单词：4个（`brim`、`butter`、`conform`、`implausible`）
- 📝 已反馈结果：5个标记为「熟悉」，2个标记为「忘记」，2个标记为「模糊」，剩余都还没学习反馈

需要我帮你筛选特定的单词列表吗？比如未完成的、新学的，或者标记为忘记的单词都可以给你列出来~
user: System: [2026-03-19 14:27:51 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548d38bd00a4b2cff63bad9c86c]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548d38bd00a4b2cff63bad9c86c",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:27 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

https://open.maimemo.com/document#/operations/maimemo.openapi.study.v1.StudyService.QueryStudyRecords
assistant: ✅ 成功获取到「查询学习记录」接口完整文档：
---
### 📌 接口基本信息
- **接口名**: `QueryStudyRecords`
- **请求方式**: POST
- **接口地址**: `https://open.maimemo.com/open/api/v1/study/query_study_records`
- **权限要求**: OAuth 2.0 认证
---
### 🎯 常见使用场景
1. 统计总单词量：传 `as_count: true` 直接返回总数
2. 查询未来某天要复习的单词：传 `next_study_date` 筛选对应日期
3. 查询特定单词的学习情况：传 `voc_ids` 或 `spellings` 按单词筛选
---
### 📥 请求参数（Body，JSON格式）
| 参数名 | 类型 | 说明 |
|--------|------|------|
| `next_study_date` | object | 按下次复习日期筛选，`start`和`end`为ISO格式时间（北京时区） |
| `voc_ids` | array[string] | 按单词ID查询，最多1000个，忽略其他条件 |
| `spellings` | array[string] | 按单词拼写查询，最多1000个，不可和`voc_ids`同时用 |
| `as_count` | boolean | 仅返回总数，不返回单词列表，适合统计 |
| `limit` | integer | 返回条数上限，最多1000，默认50 |
---
### 📤 返回结构
```json
{
  "count": 114514, // 匹配结果总数，as_count=true时只返回这个
  "records": [
    {
      "voc_id": "单词ID",
      "voc_spelling": "单词拼写",
      "add_date": "添加日期",
      "first_study_date": "首次学习日期",
      "last_study_date": "上次学习日期",
      "next_study_date": "下次复习日期",
      "last_response": "上次反馈结果",
      "study_count": 学习次数,
      "tags": "标签，STICKING(坚持中)/WELL_FAMILIAR(熟知)"
    }
  ]
}
```
---
需要我帮你调用这个接口吗？比如查你明天要复习的单词数、总单词量都可以哦~😉
user: System: [2026-03-19 14:29:33 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548d32032c48b39e7590a496b96]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548d32032c48b39e7590a496b96",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:29 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

调用
assistant: ✅ 接口调用成功！
📊 你正在学习的单词总量：**2896个**

需要我帮你查其他内容吗？比如：
1. 明天需要复习的单词数
2. 标记为「忘记」的单词列表
3. 最近一周学习的新单词
4. 特定单词的学习情况
user: System: [2026-03-19 14:33:09 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548dc49cb0b0b10c0c701e21b9c]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548dc49cb0b0b10c0c701e21b9c",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:33 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

将token写入.zshrc,上面三个接口制作成技能
assistant: ✅ 墨墨API技能制作完成啦！
---
### 🎉 已完成配置：
1. Token已写入`~/.zshrc`环境变量`MAIMEMO_ACCESS_TOKEN`
2. 三个命令已制作完成，存放在`~/.openclaw/workspace/skills/maimemo-api/`
3. 已添加执行权限，路径已加入系统PATH

### 📝 使用方法（新开终端即可直接运行）：
| 命令 | 功能 |
|------|------|
| `maimemo-progress` | 查看今日学习进度、完成率、学习时长 |
| `maimemo-today [limit] [--finished true/false] [--new true/false]` | 查看今日学习单词列表，支持筛选已完成/新学单词 |
| `maimemo-records [--count] [--date YYYY-MM-DD] [--limit 100]` | 查询学习记录，支持统计总单词量、指定日期待复习单词 |

> 刚才调用的时候显示null是因为你太久没打开墨墨APP同步了，打开APP刷一下同步就能正常显示数据啦~😉
user: System: [2026-03-19 14:36:51 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548dd6e7d8b0b376d4cc50e7b89]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548dd6e7d8b0b376d4cc50e7b89",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:36 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

给这个技能这对应的说明文件
assistant: ✅ 技能说明文件已全部完成：
1. **`SKILL.md`** - OpenClaw系统识别用的技能元数据，已配置完成，系统会自动识别该技能，后续你提到「墨墨」「背单词」「学习进度」等关键词时会自动调用相关能力
2. **`README.md`** - 详细使用说明书，包含所有命令的参数说明、使用示例、常见问题解答，你可以随时查看~

后续如果需要调整技能功能或者补充说明内容随时告诉我就行😉
user: System: [2026-03-19 14:38:59 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548deee160b0b2c3e66af88a773]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548deee160b0b2c3e66af88a773",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:38 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

查看已经安装的技能
assistant: ✨ 已安装的技能清单（共18个，含1个本地自定义技能）：
---
### 📦 从SkillHub商店安装（17个）
| 技能名 | 版本 | 功能说明 |
|--------|------|----------|
| agent-browser | 0.2.0 | 无头浏览器自动化工具，支持网页交互、抓取 |
| auto-updater | 1.0.0 | 技能自动更新工具 |
| find-skills | 0.1.0 | 技能发现与安装工具 |
| github | 1.0.0 | GitHub CLI 交互工具，支持issue/PR/CI操作 |
| gog | 1.0.0 | GOG游戏平台管理工具 |
| humanizer | 1.0.0 | AI生成文本人性化工具，去除AI写作特征 |
| ima-skills | 1.0.1 | IMA个人笔记服务API，支持笔记管理 |
| macos-desktop-control | 1.0.0 | macOS桌面控制工具 |
| memory-manager | 1.0.0 | 本地内存管理工具，支持语义搜索、快照 |
| ontology | 0.1.2 | 类型化知识图谱工具，支持实体管理、关系关联 |
| openai-whisper | 1.0.0 | 本地语音转文字工具（无需API密钥） |
| proactive-agent | 3.1.0 | 主动智能体能力包 |
| self-improving-agent | 1.0.11 | 自学习能力包，支持错误修正、经验沉淀 |
| skill-creator | 0.1.0 | 自定义技能创建工具 |
| skill-vetter | 1.0.0 | 技能安全审查工具 |
| summarize | 1.0.0 | 内容摘要工具 |
| video-frames | 1.0.0 | 视频帧/短片提取工具 |
---
### 🛠️ 本地自定义开发（1个）
| 技能名 | 功能说明 |
|--------|----------|
| maimemo-api | 墨墨背单词开放API工具，支持查询学习进度、今日单词、学习记录 |

> 自定义技能可直接在终端使用对应的命令，也可以直接和我说关键词调用哦😉
user: System: [2026-03-19 14:42:39 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548de33fd4a4b3f0d4b84a4a938]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548de33fd4a4b3f0d4b84a4a938",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:42 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

具体是怎么制作技能？
assistant: 制作自定义技能非常简单，完全不需要复杂的配置，你可以按照这个标准流程来做（刚才的墨墨技能就是这么做的哦）：
---
### 📦 技能基本结构
每个技能就是一个独立的文件夹，存放在`~/.openclaw/workspace/skills/`目录下，结构如下：
```
你的技能名/
├─ SKILL.md       # 【必填】OpenClaw系统识别用的元数据文件
├─ 命令1          # 【必填】可执行脚本，比如刚才的maimemo-progress
├─ 命令2          # 可选，一个技能可以包含多个命令
└─ README.md      # 可选，给用户看的使用说明书
```
---
### 📝 每一步详细说明
#### 1️⃣ 第一步：创建技能文件夹
在`~/.openclaw/workspace/skills/`下新建一个和技能名对应的文件夹，比如刚才的`maimemo-api`。

#### 2️⃣ 第二步：写`SKILL.md`（系统识别用）
这个文件是让OpenClaw能识别到这个技能的关键，格式是固定的：
```yaml
---
name: 技能名称
description: 技能描述，说明这个技能是干嘛的
read_when:
  - 触发关键词1，比如"查询墨墨学习进度"
  - 触发关键词2，比如"墨墨背单词"
---
# 这里可以写技能的详细说明，和README功能类似
```
只要符合这个格式，OpenClaw就会自动识别到这个技能，用户提到`read_when`里的关键词时会自动触发。

#### 3️⃣ 第三步：写可执行脚本
就是实际干活的命令，可以用任何你熟悉的语言写（Bash、Python、Node.js都可以），写完之后要加可执行权限：
```bash
chmod +x 你的脚本名
```
比如刚才的墨墨技能，我用Bash写了3个脚本，分别对应3个功能。

#### 4️⃣ 第四步：配置全局可用
把技能文件夹的路径加到系统`PATH`环境变量里，这样你在任何地方都能直接调用命令：
```bash
echo 'export PATH="$HOME/.openclaw/workspace/skills/你的技能名:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

#### 5️⃣ 第五步（可选）：写`README.md`
给用户看的使用说明，包含命令参数、示例、常见问题就行，方便后续自己用或者分享给别人。
---
### ✨ 小提示
- 脚本里可以直接读取环境变量，比如刚才的墨墨token就是存在`MAIMEMO_ACCESS_TOKEN`环境变量里，脚本直接用就行
- 一个技能可以包含多个命令，比如你做一个天气技能，可以同时有`weather-now`（当前天气）和`weather-forecast`（天气预报）两个命令
- 不需要发布，本地写完就能直接用，也可以分享给其他OpenClaw用户

如果你想做什么技能，直接告诉我需求，我可以帮你快速生成哦😉
user: System: [2026-03-19 14:47:05 GMT+8] Feishu[default] DM | ou_7f5c8f2774475eabd071360f959caf5e [msg:om_x100b548df05c4cacb4a6f224d7f60fb]

Conversation info (untrusted metadata):
```json
{
  "message_id": "om_x100b548df05c4cacb4a6f224d7f60fb",
  "sender_id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "sender": "ou_7f5c8f2774475eabd071360f959caf5e",
  "timestamp": "Thu 2026-03-19 14:47 GMT+8"
}
```

Sender (untrusted metadata):
```json
{
  "label": "ou_7f5c8f2774475eabd071360f959caf5e",
  "id": "ou_7f5c8f2774475eabd071360f959caf5e",
  "name": "ou_7f5c8f2774475eabd071360f959caf5e"
}
```

三个脚本是什么样子
assistant: 我把三个脚本的完整内容都贴给你，你可以直接修改或者参考写法：
---
### 1. `maimemo-progress`（获取今日学习进度）
```bash
#!/bin/bash

# 墨墨背单词 - 获取今日学习进度
curl --request POST \
  --url https://open.maimemo.com/open/api/v1/study/get_study_progress \
  --header 'Accept: application/json' \
  --header "Authorization: Bearer $MAIMEMO_ACCESS_TOKEN" \
  --header 'Content-Type: application/json' | jq -r '
"✅ 今日学习进度：
已完成单词：\(.data.progress.finished // 0) 个
今日目标：\(.data.progress.total // 0) 个
完成进度：\(if (.data.progress.total // 0) > 0 then (.data.progress.finished * 100 / .data.progress.total | tostring) + "%" else "0%" end)
学习时长：\(if (.data.progress.study_time // 0) > 0 then (.data.progress.study_time / 1000 / 60 | floor | tostring) + " 分 " + (.data.progress.study_time / 1000 % 60 | floor | tostring) + " 秒" else "0 分 0 秒" end)"
'
```
> 逻辑说明：用curl调用接口，拿到JSON结果后用`jq`工具格式化成人能看懂的文字输出，`// 0`是处理null值的容错逻辑。

---
### 2. `maimemo-today`（获取今日学习单词列表）
```bash
#!/bin/bash

# 墨墨背单词 - 获取今日学习单词列表
LIMIT=200
IS_FINISHED=""
IS_NEW=""

# 解析命令行参数
while [[ $# -gt 0 ]]; do
  case $1 in
    --finished)
      IS_FINISHED="$2"
      shift 2
      ;;
    --new)
      IS_NEW="$2"
      shift 2
      ;;
    *)
      LIMIT="$1"
      shift
      ;;
  esac
done

# 构造请求体JSON
BODY="{\"limit\": $LIMIT"
if [ ! -z "$IS_FINISHED" ]; then
  BODY="$BODY, \"is_finished\": $IS_FINISHED"
fi
if [ ! -z "$IS_NEW" ]; then
  BODY="$BODY, \"is_new\": $IS_NEW"
fi
BODY="$BODY}"

# 调用接口并格式化输出
curl --request POST \
  --url https://open.maimemo.com/open/api/v1/study/get_today_items \
  --header 'Accept: application/json' \
  --header "Authorization: Bearer $MAIMEMO_ACCESS_TOKEN" \
  --header 'Content-Type: application/json' \
  --data "$BODY" | jq -r '
"📋 今日学习单词（共\(.data.today_items | length)个）：
\(.data.today_items[] | "-\(.voc_spelling) \(.is_new ? "🆕" : "") \(.is_finished ? "✅" : "⏳") \(.first_response // "未学习")")
'
```
> 逻辑说明：先解析用户传的参数（比如筛选已完成/新学单词），然后动态构造请求体，调用接口后输出带标记的单词列表。

---
### 3. `maimemo-records`（查询学习记录）
```bash
#!/bin/bash

# 墨墨背单词 - 查询学习记录
AS_COUNT=false
LIMIT=100
DATE=""

# 解析命令行参数
while [[ $# -gt 0 ]]; do
  case $1 in
    --count)
      AS_COUNT=true
      shift
      ;;
    --date)
      DATE="$2"
      shift 2
      ;;
    --limit)
      LIMIT="$2"
      shift 2
      ;;
    *)
      shift
      ;;
  esac
done

# 构造请求体JSON
BODY="{\"limit\": $LIMIT, \"as_count\": $AS_COUNT"
if [ ! -z "$DATE" ]; then
  BODY="$BODY, \"next_study_date\": {\"start\": \"${DATE}T00:00:00+08:00\", \"end\": \"${DATE}T23:59:59+08:00\"}"
fi
BODY="$BODY}"

# 调用接口
RESPONSE=$(curl --request POST \
  --url https://open.maimemo.com/open/api/v1/study/query_study_records \
  --header 'Accept: application/json' \
  --header "Authorization: Bearer $MAIMEMO_ACCESS_TOKEN" \
  --header 'Content-Type: application/json' \
  --data "$BODY")

# 根据参数不同格式化输出
if [ "$AS_COUNT" = true ]; then
  echo "📊 总学习单词量：$(echo $RESPONSE | jq -r '.data.count') 个"
else
  if [ ! -z "$DATE" ]; then
    echo "📅 $DATE 需要复习的单词（共$(echo $RESPONSE | jq -r '.data.records | length')个）："
  else
    echo "📋 学习记录（共$(echo $RESPONSE | jq -r '.data.records | length')个）："
  fi
  echo $RESPONSE | jq -r '.data.records[] | "-\(.voc_spelling) | 学习次数：\(.study_count) | 下次复习：\(.next_study_date[0:10])"'
fi
```
> 逻辑说明：支持三种查询模式：统计总数/查指定日期待复习/查最近记录，根据参数不同输出不同的内容。

---
你如果想修改输出格式或者加新功能，直接改这些脚本就行，改完立刻生效不需要重启~😉
