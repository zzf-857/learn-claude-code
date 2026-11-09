---
chapter: s01
status: 进行中
tags:
  - learn-claude-code
  - agent-loop
---

# s01 — Agent Loop

**课程**：[README](../s01_agent_loop/README.zh.md) · [code.py](../s01_agent_loop/code.py)

## 这一章解决什么问题

模型只会「说出命令」，不会自动执行并把结果喂回对话；本章用 `while True` + `tool_result` 去掉人肉中间层。

## 相对上一章多了什么

（第一章）最小 harness：一个 `bash` 工具 + `agent_loop`。

## 一句话机制

有 `tool_use` 就执行并追加结果；没有就结束回合。

## 代码锚点

- `agent_loop`：`s01_agent_loop/code.py`
- 停止条件：`if not tool_calls: return`
- 外层 REPL：`history` 引用传递、累积 `messages`

## 实验与运行日志

```powershell
pip install -r requirements.txt
cp .env.example .env   # 填 ANTHROPIC_API_KEY、MODEL_ID
python s01_agent_loop/code.py
```

Prompt 建议：

1. `Create a file called hello.py that prints "Hello, World!"`
2. `List all Python files in this directory`
3. `What is the current git branch?`

记录：共几轮 `$ 命令`、最后一轮是否无工具调用。

## 自测

- [ ] 能画出 User → LLM → Tool → tool_result 回流图
- [ ] 能解释为何 `tool_use_id` 必须对齐

## 疑问与延伸阅读

← [[00-学习地图]] · 下一章 → [[s02-tool-use]]
