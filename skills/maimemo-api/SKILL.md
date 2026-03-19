---
name: 墨墨背单词开放API
description: 墨墨背单词开放API调用工具，支持获取学习进度、今日学习单词、查询学习记录
read_when:
  - 查询墨墨背单词学习数据
  - 统计学习进度
  - 获取待复习单词
---

# 墨墨背单词 API 技能

## 功能说明
封装墨墨开放API三个核心接口，快速查询学习数据

## 命令使用

### 1. 获取今日学习进度
```bash
maimemo-progress
```
返回今日已完成单词数、目标总数、学习时长

### 2. 获取今日学习单词列表
```bash
maimemo-today [limit] [--finished true/false] [--new true/false]
```
- `limit`: 可选，返回条数上限，默认200
- `--finished true`: 仅返回已完成单词
- `--new true`: 仅返回今日新学单词

### 3. 查询学习记录
```bash
maimemo-records [--count] [--date YYYY-MM-DD] [--limit 100]
```
- `--count`: 仅返回总单词数
- `--date YYYY-MM-DD`: 查询指定日期需要复习的单词
- `--limit`: 返回条数上限，默认100

## 配置说明
Token已自动写入`~/.zshrc`的`MAIMEMO_ACCESS_TOKEN`环境变量，无需额外配置
