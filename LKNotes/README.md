# LKNotes — Learn Claude Code 学习笔记库

本目录是本仓库内的 **Obsidian 库**，笔记随 Git 同步到你的 fork（`origin`），便于多设备继续学习。

## 打开方式

1. 安装 [Obsidian](https://obsidian.md/)
2. **打开文件夹作为库** → 选择仓库根下的 `LKNotes`（不要选整个 `learn-claude-code`）
3. 另一台设备：`git pull` 后即可在同一库中继续编辑

## 目录约定

| 路径 | 用途 |
|------|------|
| `00-学习地图.md` | 总览与章节索引 |
| `sNN-*.md` | 按课程章节（s01–s17）的笔记 |
| `templates/` | 笔记模板 |
| `assets/` | 截图、导出图（随笔记提交） |
| `daily/` | 可选：按日学习记录 |

## 链接课程源码

库外文件请用 **Markdown 相对链接**（Obsidian 可点击打开）：

```markdown
[s01 课程 README](../s01_agent_loop/README.zh.md)
[s01 源码](../s01_agent_loop/code.py)
```

章节笔记内用 `[[wikilink]]` 互链即可。

## Git 与 upstream

- 笔记只推送到你的 **origin**，不要向 `shareAI-lab/learn-claude-code` 提 PR 带 `LKNotes/`。
- 同步官方课程：`git fetch upstream` → `merge upstream/main`，与笔记目录一般不会冲突。

## 安全

勿在笔记中写入 API Key、`.env` 内容或不可公开的内部信息（fork 若为公开仓库会被他人看到）。
