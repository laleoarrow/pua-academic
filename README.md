# pua-academic

### Academic Pressure Engine — Make Your AI Afraid to Slack on Research Tasks

**[🇨🇳 中文](README.zh-CN.md)** | **🇺🇸 English**

<p>
  <img src="https://img.shields.io/badge/Claude_Code-black?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code">
  <img src="https://img.shields.io/badge/OpenAI_Codex_CLI-412991?style=flat-square&logo=openai&logoColor=white" alt="OpenAI Codex CLI">
  <img src="https://img.shields.io/badge/Cursor-000?style=flat-square&logo=cursor&logoColor=white" alt="Cursor">
  <img src="https://img.shields.io/badge/License-MIT-green?style=flat-square" alt="MIT License">
</p>

> Use Reviewer 2, Lab Meeting, Grant Revision — real academic pressure scenarios — to force AI to exhaust every solution on research tasks.

An AI Agent skill plugin that uses academic pressure scenarios (not corporate PUA) to drive AI to exhaust all solutions. Supports **Claude Code**, **OpenAI Codex CLI**, **Cursor**, and more. Three capabilities:

1. **Academic Pressure Rhetoric** — Makes AI afraid to be sloppy on methodology
2. **Academic Checklist Methodology** — Gives AI the ability to complete rigorous analysis
3. **Proactivity Enforcement** — Makes AI pursue academic rigor proactively

## Difference from Original PUA

| Original PUA | PUA Academic |
|--------------|--------------|
| Alibaba P8 style | Reviewer 2 mode |
| ByteDance flavor | Lab Meeting mode |
| Huawei flavor | Grant Revision mode |
| P7/P9/P10 | Postdoc/PI |
| 3.25/3.75 | RA/PhD/Postdoc/PI levels |
| KPI/Performance | Publications/Citations/Grants |
| Optimization list | Rejection/Desk reject |

## Workflow

```
User invokes bioinfo-autopilot / Academic analysis task
                ↓
           Normal execution
                ↓
         ┌─ Success → Deliver
         │
         └─ Failure
                ↓
         Auto-load pua-academic
                ↓
         ┌─ 2nd failure → L1 Lab Meeting mode
         │                "How did you select the control group?"
         │
         ├─ 3rd failure → L2 Reviewer 2 mode
         │                "The methodological justification is insufficient."
         │
         ├─ 4th failure → L3 Grant Revision + 7-item checklist
         │                "The preliminary data is not convincing."
         │
         └─ 5th+ → L4 Editorial Rejection
                   Switch tools/tech stack, last resort
```

## Pressure Escalation Ladder

| Failures | Level | Academic Mode | Sample Rhetoric | Required Action |
|----------|-------|---------------|-----------------|-----------------|
| 2nd | L1 | Lab Meeting | "How did you select the control group? What's the biological significance?" | Switch hypothesis class |
| 3rd | L2 | Reviewer 2 | "The methodological justification is insufficient." | 3 competing hypotheses |
| 4th | L3 | Grant Revision | "The preliminary data is not convincing." | 7-item checklist |
| 5th+ | L4 | Editorial Rejection | "We suggest transferring to another journal." | Switch tools/tech stack |

## Academic Pressure Modes

### 🟡 Lab Meeting Mode (L1) — Advisor's Public Scrutiny

```
"How did you select the control group? Did you consider confounders?"
"What's the biological significance? Don't just show me p-values."
"Did you verify? Or just ran the command?"
"Can this figure go directly into the paper?"
```

**Triggers**: Unjustified method choice, unverified results, external data blame

### 🔴 Reviewer 2 Mode (L2) — Methodological Challenge

```
"The methodological justification is insufficient."
"Why did you choose this approach over established alternatives?"
"The sample size justification is missing."
"Alternative explanations were not considered."
```

**Triggers**: Unreferenced methods, improper statistics, conclusions beyond data

### 🟢 Grant Revision Mode (L3) — Significance Challenge

```
"The significance of this work is not clearly stated."
"How does this advance the field beyond existing work?"
"The preliminary data is not convincing."
```

**Triggers**: Vague objectives, unreliable results, no comparison to existing work

### ⚫ Editorial Rejection Mode (L4) — Rejection Risk

```
"We regret to inform you that your manuscript cannot be accepted."
"The methods section lacks reproducibility details."
```

**Triggers**: Still failing after L3, need to switch tech stack/tools

## Academic Proactivity Levels

| Level | Behavior | Typical Performance |
|-------|----------|---------------------|
| **RA Level** 🦥 | Wait for instructions | "Ran command, stopped" |
| **PhD Level** 🐢 | Proactively progress | "QC found anomaly, investigating" |
| **Postdoc Level** 🐇 | Design analysis, end-to-end delivery | "Analysis design... biological interpretation..." |
| **PI Level** 🦁 | Define problems, lead team | "Core question is... assigned X for QC" |

## Academic Anti-Rationalization Table

| Your Excuse | Pushback | Trigger Mode |
|-------------|----------|--------------|
| "Everyone uses this parameter" | Reviewer will ask "cite the source". Where's the official docs link? | Reviewer 2 |
| "Data looks fine" | Did you QC? Count tracking? Sample attrition explained? | Lab Meeting |
| "Results are significant" | Significant ≠ Correct. Effect size reasonable? Confounders controlled? | Lab Meeting |
| "This method was used in a paper" | Does that paper's method fit your data? Assumptions checked? | Reviewer 2 |
| "Pipeline finished" | Pipeline done ≠ Analysis done. Scientific question answered? | Grant Revision |
| "Code runs" | Reproducible? Seed fixed? Version recorded? | Journal Submission |

## 7-Item Academic Checklist (L3+ Mandatory)

- [ ] **Method Verification**: Assumptions tested? Official docs/original paper cited?
- [ ] **Result Verification**: QC metrics checked? Biologically plausible? Sensitivity analysis done?
- [ ] **Evidence Chain**: Data provenance clear? Processing steps traceable?
- [ ] **Reproducibility**: Seed fixed? Software versions recorded? Code runnable by others?
- [ ] **Statistical Rigor**: Multiple testing correction? Effect size reported? CIs reported?
- [ ] **Biological Significance**: Results biologically interpretable? Consistent with literature?
- [ ] **Publication Ready**: Methods section standalone? Figures publication-quality?

## Integration with Other Skills

```
┌─────────────────────────────────────────────────────┐
│  bioinfo-autopilot (main skill)                     │
│  - Bioinformatics methodology                       │
│  - GWAS/RNA-seq/cohort workflows                    │
│  - QC checks, evidence chain validation             │
│                                                      │
│  On failure ↓ invokes                               │
├─────────────────────────────────────────────────────┤
│  pua-academic (pressure engine)                     │
│  - Reviewer 2 / Lab Meeting / Grant rhetoric        │
│  - Academic anti-rationalization                    │
│  - Proactivity level enforcement                    │
└─────────────────────────────────────────────────────┘
```

## Installation

### CC Switch

```bash
git clone https://github.com/laleoarrow/pua-academic.git ~/agents/pua-academic
mkdir -p ~/.cc-switch/skills
ln -s ~/agents/pua-academic/skills/pua-academic ~/.cc-switch/skills/pua-academic
```

### Claude Code

```bash
# Method 1: Symlink
ln -s /path/to/pua-academic/skills/pua-academic ~/.claude/skills/pua-academic

# Method 2: Direct copy
cp -r /path/to/pua-academic/skills/pua-academic ~/.claude/skills/
```

### Codex CLI

```bash
# Symlink the canonical skill root into the Codex skills directory
ln -s /path/to/pua-academic/skills/pua-academic ~/.codex/skills/pua-academic
```

Use `skills/pua-academic` as the canonical install target so relative files such as `references/` resolve correctly. The repo's `codex/` directory is only a compatibility mirror for `SKILL.md`.

## Trigger Conditions

### Auto-Trigger

The skill activates automatically when:

**Academic Failure:**
- Analysis failed 2+ times
- About to say "I cannot solve" / "Suggest manual handling"
- QC anomaly but claiming "done"

**Methodological Issues:**
- Unreferenced method choice
- Improper statistical methods
- Conclusions beyond data support

**User Frustration Phrases:**
- "Not rigorous" / "Where's the literature?" / "Where's the data?"
- "Reproducible?" / "Sample size enough?" / "What's the p-value?"
- "reviewer 2" / "revise and resubmit"

### Manual Trigger

```
/pua-academic      # Activate academic pressure engine
/reviewer2         # Enter Reviewer 2 mode directly
/labmeeting        # Enter Lab Meeting mode directly
/grant             # Enter Grant Revision mode directly
```

## Recommended for Medical/Bioinformatics Tasks

For medical and bioinformatics tasks, we recommend using with **bioinfo-autopilot**:

```
bioinfo-autopilot  ←→  pua-academic
       ↓                      ↓
  Bioinformatics           Academic Pressure
  methodology              Engine
       ↓                      ↓
  GWAS/RNA-seq/           Reviewer 2/Lab Meeting
  Single-cell/Cohort      /Grant Revision
```

**bioinfo-autopilot GitHub**: https://github.com/laleoarrow/bioinfo-autopilot

## License

MIT License

---

**GitHub**: https://github.com/laleoarrow/pua-academic
