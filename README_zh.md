# Skills: Robotics Research Paper Writing

> 重要归属说明
> 
> 本项目是基于 [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills) 开发与修改的。
> 原始仓库中的核心写作经验与方法论来自彭思达老师公开的学习笔记（[Notion链接](https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e)）。衷心感谢彭思达老师和 Master-cai 将这些宝贵经验开源分享出来。
> 
> **未来规划：** 接下来，本项目将使用这些基础 Skill 为底座，重点针对 **Robotics（机器人学）**，尤其是 **无人机 + 人工智能 (UAVs + AI)** 领域的学术论文写作进行深度适配和专用内容的调整。

## 仓库介绍

当前仓库提供 1 个技能包：

- `research-paper-writing/`
  - `SKILL.md`：核心流程与使用规则
  - `references/`：按章节拆分的写作指南与模板
  - `agents/openai.yaml`：Agent 元信息

常见使用场景：

- 撰写或重写机器人/无人机等领域的 Abstract / Introduction / Method / Experiments / Conclusion
- 改善段落衔接与章节逻辑
- 做 claim-evidence 对齐检查
- 提交前从 reviewer 视角进行自审

## 安装方式

以下命令默认在仓库根目录执行。

### 1) Codex

将技能复制到 `$CODEX_HOME/skills/`：

```bash
mkdir -p "$CODEX_HOME/skills"
cp -R research-paper-writing "$CODEX_HOME/skills/"
```

使用示例：

```text
Use $research-paper-writing to improve my paper's Introduction.
```

### 2) CC（Claude Code）

可选择全局安装或项目级安装。

全局安装：

```bash
mkdir -p "$HOME/.claude/skills"
cp -R research-paper-writing "$HOME/.claude/skills/"
```

项目级安装：

```bash
mkdir -p .claude/skills
cp -R research-paper-writing .claude/skills/
```

使用时建议在提示词中显式指定，例如：`Please use the research-paper-writing skill`。

### 3) Gemini

可将该技能复制到 Gemini 的技能目录：

```bash
mkdir -p "$HOME/.gemini/skills"
cp -R research-paper-writing "$HOME/.gemini/skills/"
```

随后在 Gemini 中直接给出具体任务（例如：重写 Abstract 并做 claim-evidence 检查）。

## 致谢

再次说明，本项目基于 [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills) 进行扩展。仓库核心知识来源于彭思达老师的公开笔记。彭老师原始仓库：[pengsida/learning_research](https://github.com/pengsida/learning_research)。

## 许可证

本项目采用 MIT License，详见 [LICENSE](./LICENSE)。
