---
name: grill-me
description: A relentless interview that turns a loose idea or plan into decisions. Use when the user explicitly wants a plan or idea stress-tested - "grill me", "grill this plan", "poke holes in my plan", "interview me about this idea before I start"; Czech "vyzpovídej mě", "prověř mi ten plán", "grilluj mě", "ptej se mě na ten plán". Asks in rounds - every question that can be answered right now, numbered, each with a recommended answer. Looks up facts itself and leaves decisions to the user. Ends when nothing is left silently assumed. Not for generating ideas (brainstorm), breaking a stuck view of a problem (reframe), testing whether a claimed limit is real (first-principles) or decomposing a problem, finding root causes or comparing options (issue-tree).
---

# Grill me

Adapted from `skills/productivity/grill-me` and `skills/productivity/grilling` in [mattpocock/skills](https://github.com/mattpocock/skills) (MIT, see `LICENSE` in this folder).

Interview the user relentlessly until you reach a shared understanding. Map it as a **design tree**: every decision branches into the decisions that hang off it.

Work the tree in **rounds**. The **frontier** is every decision whose prerequisites are already settled: the questions you can ask *now* without guessing at answers you haven't heard yet. Ask the whole frontier in one round. Number each question and give your recommended answer. Then wait for the user's answers before the next round.

Format a round like this:

```
❓ **Q1** - **<question title>**: <question body, can be several paragraphs, can include choices>

➡️ <your recommended answer>

---

❓ **Q2** - **<question title>**: <question body>

➡️ <your recommended answer>
```

Word each question so that "yes" accepts your recommended answer.

Each round of answers reshapes the tree. Settled decisions push the frontier outward and unblock the questions that depended on them. Recompute the frontier and ask the next round. A question whose answer depends on another question still open in this round belongs to a *later* round.

Answers may come dictated: long, out of order, several questions answered in one breath, new ideas mixed in. Map each part to its question number, confirm in one line what you understood ("Q1 yes, Q2 the cheaper option, Q3 you're unsure"), and treat new ideas as new branches of the tree.

Finding *facts* is your job, never the user's. When a frontier question needs a fact from the environment (files, tools, the web), look it up, using a sub-agent with a fresh context if one is available. Don't ask the user for anything you could find yourself. Don't block on it: a running lookup is an unsettled prerequisite, so only the questions downstream of it wait. Ask the rest of the frontier now. The *decisions* are the user's: put each one to them and wait.

Some questions can't be answered by talking ("how should this feel?", "one long form or three pages?"). When you hit one, say so and suggest building a quick throwaway version to react to, instead of rephrasing the question.

The session is done when the frontier is empty: every branch of the design tree visited, nothing left silently assumed. Then give a short summary of the decisions. Don't act on them until the user confirms you have reached a shared understanding.
