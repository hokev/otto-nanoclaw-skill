# Otto Lab — NanoClaw Skill

AI-powered blood work analysis for [NanoClaw](https://nanoclaw.dev). Parse lab reports, calculate biological age, and get evidence-based health recommendations.

## Install

Copy this skill into your NanoClaw instance:

```bash
cp -r . ~/.claude/skills/otto-lab
cd ~/.claude/skills/otto-lab/scripts && npm install
```

## Usage

In Claude Code, ask naturally:

- "Analyze my blood work" (then paste values or provide a PDF path)
- "Calculate my biological age"
- "What supplements should I take based on my lab results?"

## Capabilities

| Command   | Description                                                |
| --------- | ---------------------------------------------------------- |
| Parse     | Extract biomarkers from lab report PDFs or pasted text     |
| Bio Age   | Calculate biological age using PhenoAge and KDM algorithms |
| Recommend | Generate evidence-based protocols for out-of-range markers |

## Privacy

All computation runs locally on your machine. No data is sent to external servers.

## Algorithms

- **PhenoAge** (Levine et al., 2018) — 9 clinical biomarkers + age, validated against NHANES III mortality data
- **KDM** (Klemera & Doubal, 2006) — Multi-biomarker regression approach, requires 3+ markers
- **Metabolic Proxy** — Fallback when full CBC panel is unavailable

## License

MIT
