# Lesson 6 — Your first project: a personal site, live on the internet

*Session 4 — we do this together. By the end you have a real URL you can send to anyone.*

**Goal**: your own website — name, short bio, a few things you're proud of — live on the internet. This is not a toy exercise: it runs the entire stack (VS Code → Claude Code → GitHub → Vercel) and the entire workflow (plan → prompt → build → verify → deploy), and it ends with proof.

## Step 0 — Decide the content (5 min, no computer)

Write on paper or in your notes: your name, one sentence about who you are, 2–4 things you want to show (projects, work, hobbies, photos — anything). A site with real content teaches; a site with "Lorem ipsum" doesn't.

## Step 1 — Create the repo

On [github.com](https://github.com): green **New** button → name it `mysite` (or anything) → keep it Public → check "Add a README" → Create.

Then get it onto your machine. In the terminal:
```
cd Desktop
git clone https://github.com/YOUR_USERNAME/mysite.git
cd mysite
```
✅ *You now have a folder that is a repo. `git status` should say "nothing to commit".*

## Step 2 — Open the workshop

```
code .        (opens this folder in VS Code — or use File → Open Folder)
claude        (in the VS Code terminal: Terminal → New Terminal)
```

## Step 3 — Plan

Say to Claude Code (your own words, this is the shape):

> "I want a simple one-page personal site about me. I'm a complete beginner. Ask me questions until you understand what I want, then propose a plan. Don't build anything yet."

Answer its questions with your Step-0 content. Read the plan. Correct anything — this is the cheap moment to change your mind. Approve it.

## Step 4 — Standing instructions

> "Before you build: write a CLAUDE.md for this project — what the site is, that I'm a beginner, and that you should explain what you're doing as you go."

Your first CLAUDE.md. Every project you ever make gets one.

## Step 5 — Build

> "Build the plan."

Watch the loop happen: files appear, commands run, it checks its own work. You don't need to understand every line. When it finishes, it will tell you how to see the site locally (usually: open a link like `http://localhost:3000` in your browser).

## Step 6 — Verify

Open the site. Look at it like a stranger would:
- Read every word out loud. Typos? Placeholder text left over?
- Make the browser window phone-narrow. Still looks right?
- Click everything clickable.

Request changes in plain, observed language: *"The heading is huge on narrow screens"*, *"Make the background warmer"*. Two or three rounds of this is normal and is exactly how the workflow is supposed to feel.

## Step 7 — Deploy

> "Commit everything with a clear message and push to GitHub."

Then on [vercel.com](https://vercel.com): **Add New → Project** → pick your `mysite` repo → Deploy (defaults are fine). Wait ~1 minute.

✅ *You have a URL like `mysite-yourname.vercel.app`. Open it on your PHONE — not your laptop. It's really on the internet.*

## Step 8 — The moment that makes it click

Back in Claude Code:

> "Change [one word / the accent color / anything small]. Commit and push."

Now watch Vercel rebuild and refresh your phone. **Edit → live in about 60 seconds, and you never touched a server.** This loop — this exact feeling — is what you now own.

## After the session

One improvement per week, each one a full plan → deploy loop:
- a photo, a projects section, a links page
- a second page ("now", "reading", "recipes" — anything)
- ask Claude: *"what are 5 small improvements we could make? Rank them by effort."*

Small, finished, shipped. ([Principle 11](05-principles.md).)

**Next**: session 5 — leveling up: skills, connecting real tools (MCP), and [where to go from here](07-references.md).
