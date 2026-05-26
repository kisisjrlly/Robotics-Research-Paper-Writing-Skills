# Skills: Robotics Research Paper Writing

[中文介绍](./README_zh.md).

> Important Attribution
> 
> This project is based on [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills). 
> The core writing knowledge and methodology in the original repository comes from Prof. Peng Sida (彭思达)'s open study notes ([Notion Link](https://pengsida.notion.site/c1a22465a0fa4b15a12985223916048e)). We sincerely thank them for openly sharing these valuable experiences.
> 
> **Future Focus:** Going forward, this project will adapt and extend this skill specifically for **Robotics**, focusing particularly on **Unmanned Aerial Vehicles (UAVs) + Artificial Intelligence (AI)** research paper writing.

## Repository Overview

This repository currently provides one skill package:

- `research-paper-writing/`
  - `SKILL.md`: core workflow and usage rules
  - `references/`: section-specific writing guides and templates
  - `agents/openai.yaml`: agent metadata

Typical use cases:

- Drafting or rewriting Abstract / Introduction / Method / Experiments / Conclusion for Robotics/UAV papers
- Improving paragraph flow and section logic
- Checking claim-evidence alignment
- Running pre-submission self-review from a reviewer mindset

## Installation

Assume you are in the repository root.

### 1) Codex

Copy the skill into `$CODEX_HOME/skills/`:

```bash
mkdir -p "$CODEX_HOME/skills"
cp -R research-paper-writing "$CODEX_HOME/skills/"
```

Usage example:

```text
Use $research-paper-writing to improve my paper's Introduction.
```

### 2) CC (Claude Code)

Use either a global or project-level installation.

Global:

```bash
mkdir -p "$HOME/.claude/skills"
cp -R research-paper-writing "$HOME/.claude/skills/"
```

Project-level:

```bash
mkdir -p .claude/skills
cp -R research-paper-writing .claude/skills/
```

In prompts, explicitly request this skill, for example: `Please use the research-paper-writing skill`.

### 3) Gemini

Copy this skill into your Gemini skills directory:

```bash
mkdir -p "$HOME/.gemini/skills"
cp -R research-paper-writing "$HOME/.gemini/skills/"
```

Then ask concrete tasks in Gemini (for example, rewriting an Abstract with claim-evidence checks).

## Credits

This project operates as an extension of [Master-cai/Research-Paper-Writing-Skills](https://github.com/Master-cai/Research-Paper-Writing-Skills).
The foundational writing methodology originates from Prof. Peng Sida's open notes. Prof. Peng's original repository: [pengsida/learning_research](https://github.com/pengsida/learning_research).

## License

This project is licensed under the MIT License. See [LICENSE](./LICENSE).
