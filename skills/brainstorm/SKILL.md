---
name: brainstorm
description: Ideation that gets past the obvious. Use when the user wants ideas, options or concepts - "brainstorm X with me", "give me ideas for...", "what could we build here", "what can I do with $500 / one afternoon / one person", "find something to automate for my colleague"; Czech "nápady na...", "vymysli...", "co se dá dělat s...", "pojďme brainstormovat", "co by šlo postavit". Four modes - open topic, hard constraints, product or tool concepts, and ideas from a short interview about someone's work. Every mode first lists and bans the ideas anyone would give, then samples from the unusual end so the list isn't ten versions of one idea. Not for breaking a stuck view of a problem (reframe), testing whether a claimed limit is real (first-principles), decomposing a problem, finding root causes or comparing options (issue-tree) or stress-testing a plan (grill-me).
---

# Brainstorm

Goal: ideas the user would not get by typing the same question into a blank chat.

## 0. Load context

Read what the user pointed at: files, earlier messages, project instructions. Find out who the ideas are for, what has been tried, and what is off limits. Generic context produces generic ideas.

The request may be dictated: long, rambling, with false starts and side stories. That is good material. Pull out the topic, the constraints and the hints about what the user already likes, and don't ask them to restate it tidily.

If the topic is too vague to produce anything specific, ask at most two questions in one message (interview mode asks its own five questions instead). Otherwise state your assumptions and go.

## 1. Pick the mode

| Signal in the request | Mode |
|---|---|
| "ideas for X", no limits given | **Open topic** |
| numbers, deadline, "only", "with just", "within", "no budget" | **Constraints** |
| "what could we build", product, feature or tool ideas | **Product** |
| ideas for a specific person's work, no problem stated yet, "what should I automate" | **Interview** |

Modes combine. Product + constraints is common.

## 2. Set the banal bar

Write the 8-10 ideas anyone would produce in 30 seconds. They are the bar to beat, not the answer. Nothing on this list, and no paraphrase of it, may appear in the final output. Show it to the user as one line so they see what was skipped.

## 3. Generate wide

Generate about 20 candidates. For each, estimate the probability (0-1) that a typical assistant would suggest it for this request. Rules:

- At least a third of the candidates have probability below 0.10. These are the tails.
- Use at least four of the open-topic moves below, in every mode. The other modes add their own rules on top.
- Every candidate is concrete: who does what. "Gamification" is a category. "Colleagues get a coffee for every task closed with a written log" is an idea.

This is working material. Keep it short (one line per candidate) and don't paste it into the answer unless the user asks.

**Open topic moves**
- Association: take a random noun and force a link.
- Inversion: how would we make this worse? Flip each answer.
- Transplant: how does another field solve the same structure? Try hospitals, airlines, games, logistics, kids' toys, restaurants.
- Extreme user: the power user, the total beginner, someone who hates it.
- Scale shift: 10x bigger, 10x smaller, 10x cheaper.
- Time shift: how would this work in 1990? In 2035?

**Constraint rules**
- Write every constraint down as hard. Don't relax it.
- For each constraint ask: what does it make easier? What is only possible because of it?
- Generate per constraint, then combine constraints.
- Kill any idea that quietly breaks a constraint.

**Product rules**
- Each concept is **Problem** (who, what hurts, how often) + **Mechanism** (how it works, in plain verbs) + **Differentiation** (why existing options don't do this).
- Banned words in the mechanism: AI, LLM, agent, platform, app, automation, dashboard, blockchain, smart. If the concept dies without the buzzword, it wasn't a concept.

**Interview rules**
- Ask five questions in one message: What is the goal of your work? Walk me through a typical week. What do you dread or put off? What eats time or money, and roughly how much? What have you already tried?
- Wait for answers. Then produce 10 concepts for tools or automations, each worth real time or money to that person. For each: the pain it removes, rough effort (S/M/L), and what they would stop doing.

## 4. Critique and cut

Score each candidate on three things: novelty (not on the banal bar, not a small variation of it), fit (respects the context and constraints), and first-step clarity (could someone start this week?).

Drop duplicates by mechanism, not by wording. Keep 5-7 (interview mode keeps 10). If tail ideas survive the critique, keep at least two and mark them as wild cards.

## 5. Output

```
**Banal bar (skipped):** a, b, c, ...

1. **<short name>** - <the idea in one or two sentences>
   Not banal because: <...>
   First step: <something doable this week>

2. ...

**Wild cards:** #4, #6
```

End with one line: offer to go deeper on one idea, or to rerun with a different move. No closing essay.

## Rules

- Six good ideas beat twenty mixed ones.
- Don't apologise for weird ideas. Label them.
- No generic advice ("do user research", "talk to customers") unless it is the actual idea, made specific.
- When the user rejects a direction, add it to the banal bar for the rest of the conversation.
- If the user wants volume on one idea, run the loop again on that idea instead of padding the list.

---

The diversity step follows Verbalized Sampling (Zhang et al., 2025): ask for a distribution with probabilities instead of one answer, then sample the tails.
