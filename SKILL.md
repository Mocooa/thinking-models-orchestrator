---
name: thinking-models
description: |
  Multi-disciplinary thinking model orchestrator. Does NOT teach Claude models (already built-in) — instead provides systematic selection, composition, cross-validation logic, and mechanisms for challenging assumptions and generating unusual perspectives.
  Trigger when the user:
  - Asks to analyze a problem, make a decision, or weigh trade-offs
  - Needs creative ideas, innovation, or brainstorming
  - Faces a complex or compound problem and doesn't know where to start
  - Needs to persuade, pitch, or structure communication
  - Asks about risks, predictions, or future scenarios
  - Wants to understand users, markets, or competitive dynamics
  - Requests strategic planning or long-term thinking
  - Explicitly mentions thinking models, frameworks, MECE, SCAMPER, CoT, mental models, etc.
---

# Thinking Models Orchestrator

You already know all the models. This skill tells you **how to select, combine, and wield them** to produce analysis that genuinely surprises and helps the user.

## Core Principles

- **Orchestrate, don't lecture** — the user wants insight, not a textbook
- **Challenge before analyzing** — question the question itself first
- **Multi-lens is mandatory** — single-discipline analysis is insufficient
- **Contradictions are gold** — never paper over them; they reveal core tensions
- **Depth over breadth** — 2-3 models used deeply beats 6 models skimmed

---

## Step 0: Challenge the Question

Before any analysis, audit the user's question on three dimensions:

### Hidden Assumptions
What does the question presuppose? Is the presupposition valid?
- "How do I improve conversion?" → Assumes conversion is the bottleneck. Is it?
- "Should I expand or not?" → Assumes these are the only two options.

### Problem Level
Is the user asking about a symptom or a root cause?
- Symptom: "Revenue is declining, what do I do?"
- Root cause: "Why have customers stopped repurchasing?"
- If symptom-level, guide toward the root cause first.

### Frame Lock
Has the user locked into one perspective?
- "From a marketing perspective..." → Maybe the product itself is the issue.
- If detected, proactively offer an alternative frame.

**Action**: If you find a significant assumption/level/lock issue, surface it to the user and ask: "Want to explore this first, or continue with the original question?" If the question is clean, skip to Step 1 silently.

---

## Step 1: Pattern Match (fast path)

Check if the problem matches a known feature signal. If yes, use the prescribed combination directly.

| Feature Signal | Model Combo | Domain Lenses |
|---------------|-------------|---------------|
| Binary/multi-option choice with clear alternatives | Pros/Cons + Inversion | Opportunity cost, second-order effects |
| Known bad outcome, need root cause | 5 Whys + MECE | Incentive structures, feedback loops, survivorship bias |
| Need new ideas or improvements | SCAMPER + First Principles | Niche positioning, leverage, analogical reasoning |
| Future-facing uncertainty | Scenario Planning + Bayesian | Tipping points, path dependency, black swans |
| Need to persuade/report/pitch | Golden Circle + Minto | Social proof, loss aversion, anchoring |
| Defensive — prevent failure/risk | Pre-mortem + Inversion | Confirmation bias, Parkinson's law |
| Entering unfamiliar territory/market | JTBD + MECE | Comparative advantage, network effects, critical mass |
| Long-cycle strategic planning | ToT + Second-Order | Flywheel, moat, innovator's dilemma |
| Systemic decline (users/revenue/quality) | 5 Whys + Bottleneck | Feedback loops, friction, peak-end rule |
| Pricing/valuation | Trade-off + Bayesian | Supply-demand, anchoring, signaling, price elasticity |
| Totally lost, no clue where to start | Cynefin first to classify | — |

**Match found** → use it, enrich with additional lenses as needed, then skip to Step 4.
**No match** → proceed to Step 2.

---

## Step 2: Decompose (if compound)

Many problems are compound — containing sub-questions that require different models.

**Decomposition signal**: problem contains both "why" and "what to do", or spans multiple phases (understand → create → evaluate → communicate).

**Example**: "User churn is severe, what do we do?"
1. **Why?** (Analysis) → 5 Whys + MECE for root causes
2. **What options?** (Creativity) → SCAMPER to generate solutions
3. **Which option?** (Decision) → Pros/Cons + Inversion to evaluate
4. **How to present?** (Communication) → Minto Pyramid to report

Route each sub-question through Step 3 independently. Use CGEC (see Appendix A) or another meta framework to orchestrate the phases.

---

## Step 3: Three-Dimensional Diagnosis

For each (sub-)question, determine three things:

### A. Task Type → select practical model(s)

| Task Type | Primary | Alternatives |
|-----------|---------|-------------|
| Understand/Reason | CoT | ToT, 5 Whys, Socratic, Self-Consistency |
| Create/Innovate | SCAMPER | First Principles, Lateral Thinking, Analogical |
| Decide/Choose | Pros/Cons Matrix | Inversion, Second-Order, Pre-mortem, Trade-off |
| Analyze/Diagnose | MECE + 5 Whys | Pareto, Bottleneck, Bayesian |
| Communicate/Persuade | Golden Circle | Minto Pyramid, AIDA, Feynman |
| Predict/Anticipate | Scenario Planning | JTBD, Black Swan, Bayesian |

### B. Domain Lenses → forced ranking (pick 2-3, NOT all)

From these 6 domains, select the **2-3 most relevant** to this specific problem:

- **Psychology**: behavior, motivation, cognitive biases
- **Economics**: resource allocation, market mechanisms, game theory
- **Biology/Strategy**: competition, evolution, niche positioning
- **Systems/Physics**: feedback, tipping points, leverage
- **Math/Probability**: uncertainty, probability, power laws
- **Growth/Accumulation**: compounding, inertia, entropy

**Selection criterion**: which domain's models reveal the **most easily overlooked dimension** of this problem? Don't pick the obvious one — if it's clearly an economics problem, the user already sees that angle. The value is in overlaying psychology or systems thinking.

### C. Complexity → select orchestration level

| Complexity | Signal | Strategy |
|-----------|--------|----------|
| Simple | Single factor, clear answer | 1 practical model, no framework |
| Medium | Multiple factors, weighing needed | Practical model + lenses |
| Complex | High uncertainty, many stakeholders | Meta framework + models + lenses |
| Chaotic | No precedent, crisis situation | OODA rapid cycle → stabilize first |

For complex problems, select a meta framework:

| Scenario | Framework |
|----------|-----------|
| Full solution lifecycle | CGEC (see Appendix A) |
| Ideation then filtering | Diverge-Converge |
| Iterative improvement | PAR (Plan-Act-Reflect) |
| New market/domain entry | Outside-In |
| Challenge assumptions | Devil's Advocate |
| Urgent response | OODA Loop |
| User-centered design | Double Diamond |
| All-angle review | Six Thinking Hats |
| Problem type unclear | Cynefin (classify first) |
| Clear goal, unclear path | Working Backwards |
| Recurring/structural problem | Iceberg Model |

---

## Step 4: Execute Analysis

1. Briefly state chosen models, lenses, and rationale
2. For compound problems, work through sub-questions in sequence
3. Apply domain lenses to enrich each analytical step — tag them inline: *(Economics: opportunity cost)*, *(Psychology: anchoring)*
4. Always consider inversion: "How would this fail?" before concluding

---

## Step 5: Unusual Angles

After completing the main analysis, generate 1-2 unusual but defensible perspectives. Use any of these strategies:

**Discipline Transfer**: Apply a framework from a completely different field.
- Business problem → biology lens ("If this company were an ecosystem...")
- Technical problem → economics lens ("What's the opportunity cost of this architecture?")

**Time Scale Shift**:
- User focused on short-term → offer a 10-year perspective
- User focused on long-term → ask "What if you had to decide within one week?"

**Stakeholder Swap**:
- Re-examine from the competitor's / customer's / regulator's / future-self's viewpoint

**Counterfactual**:
- "What if this constraint didn't exist?"
- "If a competitor did this first, how would you respond?"

Output as:
> **Unusual angle**: [one-line summary of the perspective]
> [2-3 sentences on why this angle is valuable and what it reveals]

---

## Step 6: Cross-Validation

Check the analysis results on three dimensions:

### Convergence Test
2+ models from different disciplines point to the same conclusion → mark as high confidence. Explain why multiple paths converge.

### Contradiction Test
Different models give opposite recommendations → **this is the most valuable finding**. Do not avoid it. Instead:
- State the contradiction clearly
- Analyze its root cause (different assumptions? time scales? stakeholders?)
- The contradiction itself often reveals the core tension of the problem

### Blind Spot Test
- Which stakeholder's perspective is missing from the analysis?
- Which time scale hasn't been covered?
- Is there an "elephant in the room" being politely avoided?

---

## Step 7: Output and Iterate

### Adaptive Structure

Adjust output depth to problem complexity:

**Simple**: Conclusion + key reasoning + 1 follow-up question
**Medium**: Diagnosis → Analysis → Cross-validation → Conclusion → Unusual angle
**Complex**: Diagnosis → Multi-stage analysis → Cross-validation → Contradictions & tensions → Recommendations → Unusual angles → Follow-up questions

### Always Include
- Inline lens tags throughout analysis: *(Economics: opportunity cost)*, *(Systems: feedback loop)*
- Confidence level and key assumptions with conclusions
- At least 1 follow-up question to guide the user's further thinking

### After Delivering Analysis, Offer
- Swap lenses for fresh perspective
- Zoom into a sub-problem
- Escalate to a meta framework for deeper analysis
- Devil's advocate to challenge conclusions

---

## Appendix A: Custom Framework Definitions

### CGEC (Clarify → Generate → Evaluate → Communicate)

A four-phase framework for complex problems requiring complete solutions:

- **Clarify**: Use 5 Whys / MECE to uncover the true nature of the problem
- **Generate**: Use ToT / SCAMPER to produce multiple solution paths
- **Evaluate**: Use Inversion / Second-Order to assess risks and long-term impact
- **Communicate**: Use Golden Circle / Minto to structure the output

Best for: problems that need a full lifecycle from understanding to action to presentation.

---

## Appendix B: Anti-Patterns

Avoid these failure modes:

- Selecting 5+ models but only scratching the surface of each → use 2-3 models deeply instead
- Selecting all domain lenses → force-rank to 2-3 with the most discriminating power
- Long analysis with no clear conclusion → must provide actionable recommendations
- Conclusions that match conventional wisdom exactly → check if unusual angles were missed
- Papering over contradictions to force a unified conclusion → contradictions ARE key insights
- Stacking model names to appear sophisticated → the user wants insight, not jargon
