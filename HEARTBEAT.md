# HEARTBEAT.md - 定时任务配置
# OpenClaw 心跳任务配置 - 默认使用本地千问 3.5 模型

## 🎯 默认模型设置
default_model: volcengine-plan/doubao-seed-2.0-pro

## 📝 心跳任务列表

# 所有定时任务已删除 - 2026-03-18
# 2026-03-18 15:04 确认清理完成：已删除 2 个遗留的 cron 任务
# - 系统健康检查（每30分钟）
# - 内存监控（每小时）
tasks: []

## 🔄 动态任务（可按需添加）
# 取消注释下方内容来启用更多任务

# - name: "每日摘要"
#   schedule: "cron 0 9 * * *"  # 每天早上9点
#   model: ollama/qwen3.5:4b
#   prompt: |
#     请生成今日摘要：
#     1. 今日日期和天气
#     2. 今日待办事项提醒
#     3. 一条正能量的问候

## 📝 使用说明
# 1. 所有任务默认使用 ollama/qwen3.5:4b 模型（本地千问3.5）
# 2. 可以单独为每个任务指定不同的 model
# 3. schedule 支持: "every Xm"(分钟)、"every Xh"(小时)、"cron 表达式"
# 4. 修改此文件后，OpenClaw 会在下次心跳时自动加载新配置
