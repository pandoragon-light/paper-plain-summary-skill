# paper-plain-summary

`paper-plain-summary` is a Codex skill for reading academic papers in plain language.

It helps Codex summarize, explain, screen, compare, rank, and judge the citation value of academic papers, PDFs, Word manuscripts, abstracts, paper lists, search results, or pasted paper text.

The default style is blunt and practical: start with the conclusion, separate evidence from interpretation, explain what the paper is useful for, and point out weak evidence or overclaims.

## What It Does

- Explains one paper quickly before deep reading.
- Screens many papers and ranks them by reading priority.
- Judges whether a paper is worth citing.
- Separates direct evidence, author interpretation, inference, and missing evidence.
- Warns about common risks in climate, environmental, machine learning, review, clinical, policy, and experimental papers.
- Answers in Chinese when the user asks in Chinese, and plain English when the user asks in English.

## Install

Clone this repository, then copy the skill folder into your Codex skills directory.

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

Restart Codex after installation so the skill can be discovered.

## Use

Example prompts:

```text
Use $paper-plain-summary to explain this paper in plain Chinese.
```

```text
Use $paper-plain-summary to screen these abstracts and tell me which ones deserve deep reading.
```

```text
Use $paper-plain-summary to judge whether this paper is suitable as a citation.
```

## Repository Layout

```text
paper-plain-summary-skill/
  paper-plain-summary/
    SKILL.md
    agents/
      openai.yaml
```

## License

MIT
