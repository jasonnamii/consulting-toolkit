# consulting-toolkit

> 🇰🇷 [한국어 README](./README.ko.md)

**Natural-language router for 25 consulting techniques across 5 lineages (structuring, problem-solving, questioning, persuasion, execution). Skip the trigger-word memorization — just describe what you want.**

## Prerequisites

- **Claude Cowork or Claude Code** environment

## Goal

Consulting toolkits like MECE, SCQA, 5 Whys, and Pyramid Principle are powerful, but remembering which one fits your situation is a bottleneck. This skill parses your natural-language intent, maps it to the right technique from 5 lineages × 5 techniques each, and applies it in a consistent input→process→output format.

## When & How to Use

Triggered by either explicit technique names (MECE, SCQA, 5Whys, Pyramid, Pareto, Stakeholder Mapping, Nudging, etc.) or natural-language intents ("structure this", "why is this failing", "persuade the exec team"). The skill picks 1–3 techniques, applies them in the fixed order (structure → solve → question → persuade → execute), and labels each output with the technique used so you can learn the mapping over time.

## Use Cases

| Scenario | Prompt | What Happens |
|---|---|---|
| Diagnose a failing business | `"Why isn'''t our revenue growing?"` | Issue Tree → 5 Whys → Pareto, with a priority list |
| Prepare an executive one-pager | `"I need a 1-page brief for the board"` | Pyramid + SCQA + Executive Summary templates |
| Resolve a team deadlock | `"The team can'''t decide on tech stack"` | Alignment Building → Decision Framework |
| Design customer interviews | `"How should I structure the user interviews?"` | Funneling → Active Listening → Probing |
| Find a novel approach | `"The usual approach is stuck"` | First Principles → How-tree |

## Key Features

- **Zero trigger-word memorization** — natural language is enough
- **5 × 5 technique catalog** — 25 McKinsey/BCG-standard methods, each defined with input→process→output
- **Fixed execution order** — structuring precedes solving precedes questioning precedes persuasion precedes execution; reverses are blocked
- **Confidence tags** — every output carries a confidence level with a one-line rationale
- **Three modes** — diagnosis (recommend), apply (run), design (chain across phases)
- **Explicit boundary with [trigger-dictionary](https://github.com/jasonnamii/trigger-dictionary)** — overlapping tools (First Principles, Nudging, Backbone, Skeleton) route to that skill when invoked by name; this skill handles the natural-language entry point

## Works With

- **[trigger-dictionary](https://github.com/jasonnamii/trigger-dictionary)** — 24 named thinking tools (Holmes, Occam, Premortem). Explicit-word entry point; this toolkit is the natural-language entry point
- **[biz-skill](https://github.com/jasonnamii/biz-skill)** — 18-axis business strategy patterns for domain-specific work
- **[meeting-engine](https://github.com/jasonnamii/meeting-engine)** — full meeting lifecycle (agenda → minutes → action items)

## Installation

```bash
git clone https://github.com/jasonnamii/consulting-toolkit.git ~/.claude/skills/consulting-toolkit
```

## Update

```bash
cd ~/.claude/skills/consulting-toolkit && git pull
```

Skills placed in `~/.claude/skills/` are automatically available in Claude Code and Cowork sessions.

## Part of Cowork Skills

This is one of 25+ custom skills. See the full catalog: [github.com/jasonnamii/cowork-skills](https://github.com/jasonnamii/cowork-skills)

## License

MIT License — feel free to use, modify, and share.
