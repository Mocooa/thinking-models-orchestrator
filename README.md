<h1 align="center">Thinking Models</h1>

<p align="center">
  <strong>Turn AI analysis from "correct but bland" into "genuinely insightful"</strong>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
  <a href="https://github.com/Mocooa/thinking-models/stargazers"><img src="https://img.shields.io/github/stars/Mocooa/thinking-models?style=for-the-badge" alt="GitHub Stars"></a>
</p>

<p align="center">
  <a href="#install">Install</a> · <a href="#see-the-difference">See the difference</a> · <a href="README_zh.md">中文版</a>
</p>

---

## Why this skill?

You ask Claude to analyze a decision, a strategy, a business problem — and you get a well-organized, perfectly reasonable answer. The kind of answer you've read a hundred times in blog posts and consulting decks.

It's not *wrong*. It's just... **not helpful**. It didn't tell you anything you didn't already know.

Here's what's missing:

- 🤔 "Should I quit my job to start a business?" → Gives you pros and cons, **never questions whether "quit vs. stay" is even the right framing**
- 📉 "Our churn rate is 15%, how do we fix it?" → Lists 8 standard tactics, **never asks whether you actually have product-market fit**
- 🎯 "Analyze our competitive landscape" → Nice SWOT table, **but no unexpected angles, no "have you considered this?"**
- 🔄 Different models agree? Great insight. Different models **contradict** each other? → **Claude just picks one and ignores the tension** — but that tension is often where the real insight lives

Claude already *knows* all the thinking models — First Principles, MECE, Inversion, Pre-mortem, JTBD, you name it. But knowing them and **systematically using the right ones in the right combination** are very different things.

**This skill is the routing logic that makes the difference.**

---

## 快速安装

```bash
npx skills add Mocooa/thinking-models
```

Works with Claude Code, Cursor, Windsurf, and [15+ other agents](https://skills.sh).

<details>
<summary>Manual install (click to expand)</summary>

```bash
mkdir -p ~/.claude/skills/thinking-models

# English
curl -o ~/.claude/skills/thinking-models/SKILL.md \
  https://raw.githubusercontent.com/Mocooa/thinking-models/main/SKILL.md

# 中文版
curl -o ~/.claude/skills/thinking-models/SKILL.md \
  https://raw.githubusercontent.com/Mocooa/thinking-models/main/SKILL_zh.md
```

Pick one language — the skill auto-triggers either way.
</details>

---

## 看看区别

**Prompt**: *"Our SaaS product has 15% monthly churn. How do we reduce it?"*

<table>
<tr><th width="50%">Without skill</th><th width="50%">With skill</th></tr>
<tr><td>

Jumps to solutions:

> *"Here are practical strategies: 1. Diagnose why customers are leaving 2. Improve onboarding 3. Monitor engagement data 4. Address pricing..."*

Correct. Also something you could Google in 5 minutes.

</td><td>

Stops and challenges the question:

> *"15% monthly churn is not 'needs improvement' — it's a crisis signal. You're losing ~85% of customers annually. The question isn't 'how to reduce churn' but 'do you have product-market fit at all?'"*

Then decomposes into 5 MECE root causes, generates targeted fixes for each, runs inversion on how each fix could fail, cross-checks across Economics / Psychology / Systems, and surfaces:

> *"What if high churn is a feature, not a bug — and the problem is your business model, not your product?"*

</td></tr>
</table>

### Benchmark (3 tests, 17 checks)

| What we checked | With skill | Without |
|---|---|---|
| **Overall pass rate** | **100%** (17/17) | 29% (5/17) |
| Challenges assumptions | ✅ Every time | ❌ Never |
| Cross-validates across disciplines | ✅ Every time | ❌ Never |
| Unusual angles | ✅ Every time | ❌ Never |
| Domain lens tags | ✅ Every time | ❌ Never |
| Structured analysis | ✅ | ✅ |
| Multiple solutions | ✅ | ✅ |

Bottom two rows: Claude does these fine on its own. Top four rows: **never happens without the skill**.

Costs ~2x tokens and ~4x time. Worth it when you need real insight, not a checklist.

---

## What it does

Claude already has all the model knowledge. This skill is just **routing logic** — it decides *when* to use *which* models and *how* to combine them.

| Step | What happens |
|------|-------------|
| 0 | **Challenge the question** — hidden assumptions, symptom vs. root cause, framing traps |
| 1 | Match against 11 problem archetypes → pick model combo |
| 2 | Break compound problems into sub-questions |
| 3 | 3D diagnosis: task type × domain lenses × complexity |
| 4 | Run the analysis, tag each insight with its source lens |
| 5 | Generate 1-2 unusual angles (discipline transfer, time flip, counterfactual) |
| 6 | Cross-validate: where do lenses agree? Where do they contradict? What's missing? |
| 7 | Shape output to match complexity |

### What's inside

| | |
|---|---|
| 🧠 **25+ practical models** | CoT, ToT, SCAMPER, First Principles, MECE, 5 Whys, Inversion, Pre-mortem, JTBD, Scenario Planning, Bayesian, and more |
| 🔭 **80+ theoretical lenses** | Across Psychology, Economics, Biology/Strategy, Systems, Math/Probability, Growth |
| 🗂️ **11 meta frameworks** | CGEC, Six Thinking Hats, Cynefin, OODA, Double Diamond, etc. |

> The skill doesn't *teach* Claude these models — it already knows them. The skill tells it **when to reach for which one, and how to combine them without being shallow**.

---

## Docs for humans

The `docs/` folder has reference materials if you want to browse the models yourself:

- [practical-models.md](docs/practical-models.md) — 25+ models with scenarios and prompt patterns
- [mental-models-library.md](docs/mental-models-library.md) — 89 models across 9 disciplines
- [meta-frameworks.md](docs/meta-frameworks.md) — 11 frameworks for combining models

These are for you to read on GitHub — the skill doesn't load them.

---

## Contributing

Found a problem? [Open an issue](https://github.com/Mocooa/thinking-models/issues). Want to improve the routing logic or add a new pattern? PRs welcome.

## License

[MIT](LICENSE)
