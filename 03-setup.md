# Lesson 3 — Setup: your workshop

*Session 2 — we do this together, step by step. Skim before; don't pre-install unless you're comfortable (steps 1–2 are safe homework after session 1).*

## The three pieces and what each does

| Tool | Role | Analogy |
|---|---|---|
| **VS Code** | The editor — where you see and edit your project's files. Claude Code runs in a panel inside it. | The workshop: bench, good lighting |
| **GitHub** | Online home of your repos: backup, history, sharing | The warehouse with a ledger of every change |
| **Vercel** | Watches your GitHub repo; every change is automatically published to the live internet | The delivery service: finished goods → shelf, automatically |

The magic circuit: **edit in VS Code → save to GitHub → Vercel publishes → your change is live in ~60 seconds.** No servers to manage; free tiers cover everything we do in this course.

## About the terminal (read this first)

The black window is the honest interface — you type a command, the computer does exactly that. It looks intimidating; it isn't. You need about five commands total:

| Command | What it does |
|---|---|
| `cd foldername` | go into a folder ("change directory") |
| `cd ..` | go up one folder |
| `ls` | list what's in the current folder |
| `claude` | start Claude Code here |
| `git status` | show what's changed in this repo |

Claude Code will teach you the rest — you can literally ask it "what does this command do?" or "which folder am I in?".

**Opening a terminal**: Mac — press Cmd+Space, type "Terminal", Enter. Windows — Start menu, type "PowerShell", Enter. Inside VS Code — menu: Terminal → New Terminal (this is the one you'll mostly use).

## Installation checklist

Do these in order. Each step says what success looks like.

### 1. Install VS Code
Go to [code.visualstudio.com](https://code.visualstudio.com), download, install, open it once.
✅ *Success: VS Code opens and shows a Welcome tab.*

### 2. Create a GitHub account
Go to [github.com](https://github.com) → Sign up. Free.
⚠️ *Your username becomes public and appears in your project URLs — pick one you're happy to show people.*
✅ *Success: you can log in and see your (empty) profile page.*

### 3. Install git
- **Mac**: open Terminal, type `git --version`, press Enter. If a popup offers to install "command line developer tools", accept and wait.
- **Windows**: install [Git for Windows](https://gitforwindows.org) with default options.
✅ *Success: `git --version` prints a version number like `git version 2.x.x`.*

### 4. Install Node.js
Go to [nodejs.org](https://nodejs.org), download the **LTS** version, install with defaults. (Node is the runtime many tools, including Claude Code, are built on. You'll never use it directly.)
✅ *Success: in a NEW terminal window, `node --version` prints a version number.*

### 5. Install Claude Code
In the terminal:
```
npm install -g @anthropic-ai/claude-code
```
Then type `claude` and press Enter — it will walk you through logging in with your Claude account.
✅ *Success: you see the Claude Code welcome screen and can type a message to it.*
💡 *First thing to try: ask it "look around this folder and tell me what's here".*

### 6. Create a Vercel account
Go to [vercel.com](https://vercel.com) → "Sign up with GitHub". (Notice what you just did: connected two tools. You'll do this a lot.)
✅ *Success: you see the empty Vercel dashboard.*

### 7. Set spending limits — before anything else
Wherever billing exists, find the usage-limit setting and set it NOW, while everything is fresh and nothing is urgent:
- Your Claude plan: check what plan you're on and what it includes.
- Any API you ever add later: set a spending cap the same day you add it.

This is a non-negotiable house rule of the course — see [Principles](05-principles.md), rule 6. Caps turn "catastrophe" into "hm, I hit my limit."

## When something goes wrong

It will, for at least one of us, and that's fine — installs are the most error-prone part of the whole course. The debugging move, which is itself lesson material:

1. Copy the ENTIRE error message (don't summarize it).
2. Paste it to Claude (chat is fine at this stage) with one sentence of context: "I was installing X on a Mac and got this."
3. Do what it says; paste the next error if there is one. Repeat.

You just learned the most important developer skill: you don't need to *understand* errors, you need to *ferry* them to something that does.

## Get the course repo

Once Claude Code works, in the terminal:
```
cd Desktop
git clone https://github.com/greenbits-dev/ai-immersion.git
cd ai-immersion
claude
```
Then ask Claude: *"I'm a student on this course. Quiz me on lesson 2."*

✅ *Success: Claude answers as a tutor. Your workshop is open.*

**Next lesson**: [The workflow](04-workflow.md) — the loop you'll run for everything, forever.
