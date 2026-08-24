# Lesson 2 — Key concepts

*Session 1. Read time: ~20 minutes. This is the densest lesson in the course — everything after it builds on these dozen words. The analogies are imperfect but load-bearing.*

## 1. LLM / model

The "brain". A large language model is a program trained on enormous amounts of text that predicts what text should come next — which turns out to be enough to converse, write, and code. Models differ in size and character:

- **Bigger models** (Opus-class): smartest, slowest, priciest. Deep reasoning, hard problems.
- **Mid models** (Sonnet-class): the daily driver. Great balance.
- **Small models** (Haiku-class): fast and cheap. Simple, high-volume tasks.

**Analogy**: hiring. Sometimes you need the senior architect, usually the solid contractor is right, and for repetitive tasks the quick apprentice is cheapest.

**Key point**: the model has *no memory* between conversations. Everything it "knows about you" has to be given to it every time. This is why the next two concepts matter more than anything.

## 2. Tokens

The units the model reads and writes — roughly word-fragments (about ¾ of a word each). Every AI service bills by tokens in + tokens out, like a utility bills by kWh.

**Why you care**: tokens are the cost meter AND the memory meter. Long conversations and big files consume tokens.

## 3. Context window — and the "dumb zone"

The context window is the model's working memory: everything it can "see" right now — your instructions, the conversation so far, files it has read. It is large but finite.

Here is the trap: performance doesn't fall off a cliff when the window fills. It *degrades gradually*. Matt Pocock calls the last stretch the **"dumb zone"** — the conversation still works, but the model starts forgetting earlier instructions, mixing things up, making sloppy mistakes.

**Analogy**: a workbench. Big, but when it's buried under every tool and offcut of the day, work gets sloppy — not impossible, just worse. The fix isn't a bigger bench; it's clearing it and laying out only what the next job needs.

**Practical rule (memorize this one)**: short, focused sessions. When a task is done, start fresh. Never push a long session "just one more thing" deep into the dumb zone.

## 4. Prompt & system prompt

A prompt is what you type. A system prompt is the standing instructions the model receives before your message — its job description. In Claude Code you control part of this through a file (CLAUDE.md, below). Good prompting for beginners is mostly: **say what you want, what "done" looks like, and what to avoid** — like briefing a very fast, very literal new hire.

## 5. Repo (repository)

A project folder with a memory. A repo holds your project's files *plus* the full history of every change ever made (via a tool called **git**). You can see what changed, when, and roll anything back.

**Analogy**: a document with unlimited, perfectly organized "track changes" — for a whole folder.

**Why it's the killer feature for AI work**: the undo button gives you courage. If Claude Code wrecks something, you roll back in one command. You will never lose work — so you can let the AI work boldly.

**GitHub** is the website where repos live online — backup, sharing, and (as you'll see) the trigger for publishing. This course itself lives in a repo on GitHub; if you're reading this file there, you're already using one.

## 6. Markdown files

Plain text files with simple formatting marks (`# heading`, `**bold**`, `- list`). No Word, no fonts, no lock-in.

**Why AI work runs on markdown**: it's text, and models are text machines. Your notes, your instructions to Claude, your plans, this very lesson — all markdown. It is the paper of the AI workshop.

## 7. CLAUDE.md — the standing instructions

A markdown file in your repo that Claude Code reads automatically at the start of every session. Whatever you write there — "this project is X", "always do Y", "never touch Z" — becomes standing orders.

**Analogy**: the laminated instruction sheet taped to the workshop wall. New assistant walks in, reads it, knows the house rules.

**This is the single highest-leverage file you'll ever write.** Teaching the file beats repeating yourself in every session. This repo has one — [open it](CLAUDE.md); it's what makes Claude act as your tutor here.

## 8. Scripts

Small programs that do one job — usually a text file of commands. Claude Code writes them constantly: "a script that renames all these photos by date". You don't need to write scripts; you need to know they exist so you can ask for one. **Rule of thumb**: doing something tedious a third time? Ask for a script.

## 9. Agents

An AI that doesn't just answer — it *acts in a loop*: try something, look at the result, adjust, try again, until the goal is met. Claude Code is an agent: ask it to fix a bug and it reads code, makes a change, runs the test, sees the failure, fixes it, reruns — like a person would.

**Analogy**: the difference between asking someone for directions (chat) and hiring a driver (agent).

## 10. Skills

Packaged know-how you (or others) give Claude Code: a folder of instructions it loads when a matching task appears — "how we write blog posts", "how we deploy". Write once, reuse forever.

**Analogy**: recipe cards in the workshop drawer. The compounding effect — every lesson you teach the system makes every future session better — is the real endgame of this course.

## 11. MCPs and APIs

- **API**: a service's official counter for programs — how software orders things from other software (weather data, sending email, taking payment). Usually metered and billed.
- **MCP**: a standard plug that connects tools to Claude — your calendar, Gmail, a database. Plug it in; Claude can now see and use that system.

**Analogy**: APIs are the service counters of every business in town; MCP is the universal adapter that lets your assistant walk up to any of them.

## 12. Hallucination

Models sometimes state false things with total confidence — plausible-sounding names, facts, numbers that don't exist. It's not lying; it's autocomplete overreaching.

**Rule**: the model is a brilliant drafter and a mediocre witness. Anything that matters — a fact, a price, a claim — gets verified. This shapes the whole workflow in [Lesson 4](04-workflow.md).

---

**Quick self-check** (answers are all above):
1. Why does a long conversation slowly get worse?
2. What gives you the courage to let AI edit your files boldly?
3. What's the difference between a prompt and CLAUDE.md?
4. Why must anything important be verified?

**Next lesson**: [Setup — your workshop](03-setup.md).
