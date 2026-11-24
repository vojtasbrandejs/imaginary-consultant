---
name: issue-tree
description: Decompose a problem, find root causes or compare options with an issue tree. Use for "why is X happening", "find the root cause", "structure this problem", "break this down", "what would it take to achieve X", "what does producing X require", "build me an issue tree", "A or B - what does each lead to"; Czech "proč se děje...", "najdi příčinu", "rozlož to", "rozhodni mezi", "co obnáší", "co z toho vyplyne". Picks a Why tree (causes -> testable hypotheses), What tree (parts -> workplan) or How tree (interventions -> ranked options), checks that branches don't overlap or leave gaps (MECE), and for decisions traces the root cause backward and each option's consequences forward. Not for generating ideas (brainstorm), breaking a stuck view of a problem (reframe), testing whether a claimed limit is real (first-principles) or stress-testing a plan (grill-me).
---

# Issue tree

Goal: turn a messy problem into a structure where every leaf can be tested or acted on.

## 1. Frame before you build

- **Key question** in one sentence: specific, actionable, with scope and time. Bad: "Improve onboarding." Good: "Why do most new colleagues stop using the tool within two weeks?"
- **Who decides**, and what they would do differently with the answer.
- **Candidate crux**: your best guess at the one sub-question that, once answered, settles most of the rest. Confirm or replace it after the MECE check in step 4.

The user may describe the problem in a long, dictated, rambling message. Extract the key question yourself and show it back in one line.

If the question can't be made specific, ask at most two questions in one message. Otherwise state your assumptions and continue.

## 2. Pick the shape

| Question | Shape | Leaves become |
|---|---|---|
| "Why is X happening?" | **Why** (diagnostic) | hypotheses with tests |
| "What does X consist of / require?" | **What** (components) | a sequenced workplan |
| "How might we achieve X?" | **How** (solutions) | ranked options |
| "A or B?" | **Decision** | causal tree (step 5) |

Say which shape you picked and why, in one line.

## 3. Build the tree

- **Level 1**: 2-5 branches split by one principle. Process steps, customer segments, a formula (revenue = volume x price), internal vs external. Name the principle.
- Go deeper until every leaf can be answered, tested or acted on. Usually three levels.
- Prune branches that don't matter, visibly: "not pursued: small impact".
- **Why tree**: each leaf is a hypothesis "X happens because Y", plus the evidence that would confirm or refute it, plus the quickest test.
- **How tree**: each leaf is an intervention, scored on impact, effort and confidence.

## 4. Check MECE

- **No overlap**: could any item sit under two branches? Tighten the splitting principle.
- **No gaps**: is there a cause or option nobody listed? Add an "other" branch only if you can say what might be in it.
- Check every level, not only the leaves.

## 5. Decisions: causal tree

**Backward** (when the decision responds to a problem). From the symptom, keep asking "why?" until you reach bedrock: a decision someone made, an outside fact, or a mechanism you can change. Branch where there are several causes. Don't force one neat chain.

**Forward.** For each live option, trace:

- **First-order consequences**: direct, within weeks.
- **Second-order consequences**: what the first-order effects cause. How people react, what happens to systems and money.
- **What it closes off**: options you lose by choosing it.

Mark each option as reversible or one-way.

## Output

Tree as indented text:

```
Key question: ...
Shape: Why | Split by: process steps | Crux: ...

1. <branch>
   1.1 <sub-branch> -> H: ... | test: ...
   1.2 ...
2. <branch>
   2.1 ...
   (not pursued: 2.3, small impact)
```

Then:

- **Top 3 hypotheses or options**, each with a test or a first step.
- **The crux**, and what answering it would change.
- **Recommendation**: one short paragraph, or "need data X first".

For a decision: the causal map, consequences per option (first-order, second-order, closes off, reversible?), and a recommendation.

## Rules

- No tree for the tree's sake. If the problem is simple, say so and answer directly.
- Facts you can look up (files, data, search), look up. Ask the user only for decisions and things only they know.
- A hypothesis without a test is a guess. Every Why leaf gets a test.

---

Issue trees and MECE come from consulting practice; see Barbara Minto, *The Pyramid Principle*.
