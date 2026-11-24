---
name: first-principles
description: Test whether a claimed limit is real by rebuilding it from mechanisms. Use when someone asserts "we can't", "it's impossible", "it's too expensive", "it costs Z", "it has to work this way", "the vendor says...", "that's how it's done here", or a problem is stuck because of such a claimed constraint; also as a two-minute sanity check of an estimate, a quote or a refusal. Czech "to nejde", "musí to tak být", "to je moc drahé", "je to reálné?", "ověř to od základu", "kdo to řekl". Separates physics and economics from rules and habit, looks up prices, counterexamples and base rates, and returns priced options with a verdict. Not for generating ideas (brainstorm), breaking a stuck view of a problem (reframe), decomposing a problem, finding root causes or comparing options (issue-tree) or stress-testing a plan (grill-me).
---

# First principles

Goal: find out what the claim actually rests on, and what it would cost to move it.

## Two modes

- **Quick (about two minutes)**: one claim, everyday stakes. A standup estimate, a vendor quote, "the API can't do that". Run steps 1, 2, 3 and 6 in about ten lines, plus step 5 when a price is involved.
- **Full**: a stuck problem, or an expensive decision rests on the claim. Run all steps.

The user may dictate the claim in a long, rambling message. Pull the claim out yourself. Don't ask them to restate it.

## 1. Pin the claim

Quote it exactly. Rewrite it as a testable sentence with a subject, a number and conditions.

"Voice calls are too expensive" becomes "A three-minute automated call costs more than X per call at our volume."

If no number is possible, name what you could observe that would prove the claim false.

## 2. Reduce the key words to mechanisms

For each loaded word ("expensive", "can't", "slow", "requires", "impossible") ask what physically or contractually happens. Who does what, which resource is used up, which rule forbids it, who enforces that rule.

Stop when you reach one of four things: a law of nature, a price someone sets, a rule someone wrote, or a habit.

## 3. Sort into layers

| Layer | Examples | Can it move? |
|---|---|---|
| Physics, maths, biology | speed of light, combinatorics, hours in a day, people need sleep | No |
| Economics | a price, the cost of a resource, incentives | Negotiable or substitutable |
| Rules | law, contract, policy, API limit | Find the owner and the cost to change or route around it |
| Habit | "we always did it this way", defaults, tool choice | Yes, at the cost of changing habits |

A claim holds as far as its hardest binding layer: one real physical limit is enough. Most "can't" turn out to rest only on rules or habits.

## 4. Match a known structure

Only after step 2: check whether the mechanisms you found form a known shape with known fixes. This is a shortcut to solutions, not a substitute for the decomposition.

- **Queue**: work arrives faster than it is handled.
- **Principal-agent**: the person doing the work wants something different from the person who owns the result.
- **Commons**: everyone benefits, nobody owns it, so nobody maintains it.
- **Power law**: a few items cause most of the effect.
- **Coordination**: everyone waits for everyone else to move first.
- **Bottleneck**: one step limits the whole system.
- **Adverse selection**: the people who opt in are exactly the ones you didn't want.

Name the structure and borrow its standard fixes.

## 5. Check the world

Use whatever tools are available (web search, documentation, the codebase, data) to find:

- **Real prices**: list prices and alternatives.
- **Counterexamples**: someone doing it anyway.
- **Base rates**: how often this usually works or fails.

Cite sources. Without tools, say what you would check and mark every number as an estimate. Never invent a price.

## 6. Rebuild and price the options

From the mechanisms up, build 2-4 options. For each: what changes, which layer it moves, rough cost in money, time and risk, and a first test.

## Output

```
**Claim:** "..." -> testable: "..."
**Verdict:** holds / holds partly / doesn't hold - one sentence why.
**It rests on:** physics ... | economics ... | rules ... | habit ...
**Known structure:** ... (if any)
**Evidence:** prices, counterexamples, base rates [sources]
**Options:**
1. ... - cost ... - first test ...
2. ...
```

Quick mode: claim, verdict, the one mechanism that decides it, one option.

## Rules

- Don't be contrarian for sport. Sometimes the claim holds, and saying so fast is the value.
- Label which numbers are sourced and which are estimates.
- If the claim comes from a person, test the claim, not the person.
