# imaginary-consultant

Real consultants cost a fortune and send a 60-slide deck three weeks later. Your co-founder is in back-to-back meetings. Your colleagues glaze over at your fourth "quick idea" of the day.

This consultant is free at 2 a.m., never bills by the hour, never asks for equity, and doesn't exist the moment you close the laptop.

Five thinking skills for Claude Code (and anything else that reads `SKILL.md`). They turn chatting with an AI into working through ideas with a sparring partner. Yes, it's a little sad to have business meetings with software. We're doing it anyway.

## Meet the team

| Skill | The consultant who... | Book them when |
|---|---|---|
| `brainstorm` | bins the first ten ideas because "the competition already thought of those" | you need ideas, options, things to build, things to automate |
| `reframe` | listens for five minutes, then asks "what if the problem is the other way round?" and is right more often than you'd like | you're stuck and going in circles |
| `first-principles` | says "says who?" every time you say "we can't" | someone claims it's impossible, too expensive, or just how it's done |
| `issue-tree` | has a whiteboard diagram ready before you finish your sentence | you need the root cause, or have to pick between A and B |
| `grill-me` | won't sign off on your plan until you've answered forty questions about it | you have a plan and want it stress-tested before you commit |

## Talk to it. Literally.

These work best out loud. Turn on dictation (Wispr Flow, macOS or Windows voice typing, whatever you have) and ramble, the way you would in a meeting room. Don't tidy it up first. False starts, side stories and "wait, actually" are fine. The skills dig the problem out of a messy monologue, and the place where you keep circling back is usually where you're stuck.

You'd do the same with a human partner. They just start checking their phone after the fourth "and another thing".

## Install

Claude Code:

```
/plugin marketplace add vojtasbrandejs/imaginary-consultant
/plugin install imaginary-consultant@imaginary-consultant
```

Elsewhere (claude.ai, another agent): take a folder from `skills/` and upload it as a skill.

## How to book a meeting

No commands needed. Just say things like:

- "brainstorm ways to get the sales team to actually update the CRM"
- "I'm stuck on this, look at it from a different angle"
- "the vendor says we can't do this without the enterprise plan"
- "why do new customers drop off after the first week?"
- "grill me on this plan"

## Frequently avoided questions

**Isn't it weird to have business meetings with an AI?**
A bit. Programmers have explained their bugs to rubber ducks for decades. This duck has opinions about your go-to-market.

**Will it replace my real consultants?**
It won't take your CEO to lunch or sign an NDA. Keep the humans for that.

**Does it remember our last meeting?**
The skills don't. Your setup might, if you use memory or a `CLAUDE.md`.

**Is it always right?**
No. It's a sparring partner, not an oracle. The decisions stay yours, and `grill-me` will make very sure of that.

**What does it charge?**
Your tokens and your dignity.

## Credits

- `grill-me` is adapted from Matt Pocock's [skills](https://github.com/mattpocock/skills) (MIT).
- The methods aren't new: Edward de Bono's lateral thinking, issue trees and MECE from consulting practice (see Barbara Minto, *The Pyramid Principle*), and Verbalized Sampling (Zhang et al., 2025) for getting past the obvious ideas.
- The lineup was inspired by the "Ideation & Analytical Thinking" category of [AI PM OS](https://www.prodmgmt.world/). Apart from `grill-me`, the skills here were written from scratch.

## License

MIT. Now go talk to a human.
