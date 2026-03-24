# pua-academic

### Academic Pressure Engine for AI Coding Agents

An AI Coding Agent skill plugin that uses academic research pressure rhetoric (deadline, peer review, advisor feedback, publication pressure) to drive AI to exhaust every possible solution before giving up. Supports **Claude Code**, **OpenAI Codex CLI**, **Cursor**, and more.

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Cursor-000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

## What is pua-academic?

Unlike the original **pua** which uses corporate PUA rhetoric (Alibaba 361, ByteDance, PIP), **pua-academic** uses academic research pressure to motivate AI:

- **Deadline Pressure**: "The paper submission deadline is tomorrow. Let's get this done."
- **Peer Review**: "Reviewer #2 would not accept this solution. Find a more rigorous approach."
- **Advisor Feedback**: "Your advisor expects better methodology. Show the complete analysis."
- **Publication Pressure**: "This needs to be conference-ready quality."

## Key Features

1. **Academic Rhetoric** — Makes AI afraid to submit incomplete work
2. **Rigorous Methodology** — Gives AI the ability to produce publication-quality output
3. **Self-Review Enforced** — AI must review its own work before claiming completion

## Installation

### Claude Code

```bash
# Manual install
git clone https://github.com/tanweai/pua-academic.git ~/.claude/plugins/pua-academic
```

### OpenAI Codex CLI

```bash
mkdir -p ~/.codex/skills/pua-academic
curl -o ~/.codex/skills/pua-academic/SKILL.md \
  https://raw.githubusercontent.com/tanweai/pua-academic/main/codex/pua-academic/SKILL.md
```

### Cursor

```bash
mkdir -p .cursor/rules
curl -o .cursor/rules/pua-academic.mdc \
  https://raw.githubusercontent.com/tanweai/pua-academic/main/cursor/rules/pua-academic.mdc
```

## Quick Start

1. Install the skill using one of the methods above
2. The skill will automatically activate when:
   - Task has failed 2+ times
   - AI is about to give up
   - User expresses frustration
3. Or manually trigger with `/pua-academic`

## Difference from Original PUA

| Aspect | PUA (Original) | PUA-Academic |
|--------|----------------|--------------|
| Rhetoric Style | Corporate PUA (Alibaba, PIP) | Academic pressure (deadline, peer review) |
| Pressure Escalation | L1-L4 corporate levels | Research milestone stages |
| Key Phrases | "3.25", "毕业", "PIP" | "Deadline", "Reviewer #2", "Advisor" |
| Target Use Case | Debugging, implementation | Research, analysis, documentation |
| Tone | Corporate pressure | Academic rigor |

## When to Use

- **Use PUA (Original)** for: Debugging, code implementation, deployment issues
- **Use PUA-Academic** for: Research tasks, literature review, documentation, analysis

## License

MIT
