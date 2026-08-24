# Lesson 4 — The workflow

*Session 3. Read time: ~10 minutes. This is the loop you'll run for everything, from fixing a typo to building a product.*

Every piece of real work follows the same shape:

```
PLAN  →  PROMPT  →  BUILD  →  VERIFY  →  DEPLOY
  ↑                                 |
  └──────── learn & repeat ─────────┘
```

## 1. Plan — before any building

Tell Claude Code what you want and explicitly ask it to **plan first, build nothing yet**:

> "I want X. Ask me questions until you understand, then propose a plan. Don't write anything yet."

Claude Code has a built-in plan mode for exactly this (press Shift+Tab to switch modes).

Better yet: **ask Claude to write the prompt.** Describe your goal messily — voice-memo quality is fine — then say:

> "Turn this into a clear, detailed brief for yourself."

It writes better prompts than beginners do; your job is just to read the plan and correct it. This one move is the biggest quality lever you have.

**Why planning is the step beginners skip and experts never skip**: a wrong plan costs a sentence to fix; wrong code costs a session.

## 2. Prompt — the brief

Approve or edit the plan; that becomes the instruction. Always include what "done" means:

> "Done = the page shows my three projects and looks right on a phone."

A brief without a definition of done is a wish, not an instruction.

## 3. Build — let it work

Claude Code edits files, runs commands, checks its own results. Watch loosely; you don't need to understand every line scrolling by. Answer its questions when it asks. If something looks alarming, you can interrupt at any time — nothing is final until you commit.

## 4. Verify — never skip

**Do not trust, check.** Open the result. Click every button. Read the text out loud. If it claims "tests pass", ask to see them run.

When something is off, report what you *observed*, concretely:

- ❌ "It's broken"
- ✅ "The menu overlaps the logo when I make the window narrow"

Concrete observations get fixed in one round; vague complaints get guesses.

## 5. Deploy — ship it

Commit (save a checkpoint into history), push to GitHub, Vercel publishes. Ask Claude to do all three: *"commit this with a clear message and push."*

Then **start a fresh session** for the next task — remember the dumb zone from [Lesson 2](02-key-concepts.md). Done → commit → new session is the rhythm.

## The loop is fractal

Five minutes for a typo. A dozen loops for a feature. A week of loops for a project. The shape never changes — which means once you've run it a few times on small things, you already know how to build big things.

**Next lesson**: [Principles](05-principles.md) — the rules that keep the loop from going wrong.
