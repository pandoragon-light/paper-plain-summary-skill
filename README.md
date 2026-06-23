# paper-plain-summary

`paper-plain-summary` 是一个用于快速阅读论文的 Codex skill。它的目标很简单：把论文、摘要、PDF、Word 手稿或论文列表读成直白、有用、能马上判断价值的人话。

`paper-plain-summary` is a Codex skill for reading academic papers in plain language. It helps Codex turn dense academic material into clear summaries, reading priorities, citation advice, and evidence-aware judgments.

## 中文介绍

这个 skill 适合这些场景：

- 想快速知道一篇论文到底讲了什么。
- 想判断一篇论文值不值得精读、引用或暂时跳过。
- 想从一批论文题目、摘要或搜索结果里筛出优先阅读对象。
- 想知道论文的证据强不强，结论有没有夸大。
- 想把英文论文用中文白话解释清楚。

它默认会先给结论，再解释问题、方法、发现、用处、引用价值和风险。它不会把作者的解释直接当成事实，也会提醒哪些地方只是推断、哪些地方还缺证据。

## English Overview

This skill is useful when you want to:

- Understand what a paper says before deep reading.
- Decide whether a paper is worth reading, citing, or skipping for now.
- Screen many titles, abstracts, PDFs, manuscripts, or search results.
- Separate direct evidence from author interpretation and model inference.
- Identify weak evidence, overclaims, missing methods, or narrow scope.

The default style is direct and practical: start with the conclusion, explain the method without jargon, judge citation value, and point out limitations.

## 功能 / What It Does

- 单篇论文速读：说明研究问题、方法、核心发现和局限。
- 批量筛选论文：按 A/B/C/D 优先级判断哪些值得精读。
- 引用价值判断：说明论文能支持什么观点，不能支持什么观点。
- 证据分层：区分论文直接支持、作者解释、合理推断和缺失证据。
- 风险提醒：关注气候环境、机器学习、综述、临床、政策和实验论文中的常见误读。
- 双语输出：用户用中文提问时用中文回答，用英文提问时用 plain English 回答。

## 安装 / Install

克隆仓库，然后把 `paper-plain-summary` 文件夹复制到 Codex 的 skills 目录。

Clone this repository, then copy the `paper-plain-summary` folder into your Codex skills directory.

PowerShell:

```powershell
git clone https://github.com/pandoragon-light/paper-plain-summary-skill.git
Set-Location .\paper-plain-summary-skill
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
Copy-Item -Recurse -Force .\paper-plain-summary "$env:USERPROFILE\.codex\skills\"
```

macOS or Linux:

```bash
git clone https://github.com/pandoragon-light/paper-plain-summary-skill.git
cd paper-plain-summary-skill
mkdir -p ~/.codex/skills
cp -R paper-plain-summary ~/.codex/skills/
```

安装后重启 Codex，让 skill 被重新发现。

Restart Codex after installation so the skill can be discovered.

## 使用示例 / Usage

```text
Use $paper-plain-summary to explain this paper in plain Chinese.
```

```text
Use $paper-plain-summary to screen these abstracts and tell me which ones deserve deep reading.
```

```text
Use $paper-plain-summary to judge whether this paper is suitable as a citation.
```

中文也可以直接这样说：

```text
用 $paper-plain-summary 帮我用白话解释这篇论文，并判断它值不值得引用。
```

```text
用 $paper-plain-summary 帮我筛选这些摘要，告诉我哪些最值得精读。
```

## 仓库结构 / Repository Layout

```text
paper-plain-summary-skill/
  paper-plain-summary/
    SKILL.md
    agents/
      openai.yaml
```

## 许可证 / License

MIT
