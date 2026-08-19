# Xiaohongshu Growth Skill

[简体中文](./README.md) · **English**

A "Xiaohongshu growth advisor" knowledge pack you install into your AI assistant. Once it is in place, you just talk to your AI in plain language —

> "I have 300 followers and 12 posts with almost no reach. What's wrong?"
> "Lay out my five posts for this week."
> "Will this title get picked up? Give me three rewrites."

It answers based on **the stage your account is actually in**, with concrete next actions instead of "be consistent, be authentic" platitudes.

The methodology is distilled from five long-form posts published by **[@yanliudreamer](https://x.com/yanliudreamer/articles)** (*Dreamer妍妍* on Xiaohongshu, 198K followers, principal AI product designer at a Silicon Valley company). This repository does not reproduce the original articles — only the executable judgments and operations drawn from them.

> **New to the platform?** Xiaohongshu (小红书, also known as RedNote) is a Chinese lifestyle and knowledge-sharing platform — roughly Instagram and Pinterest crossed with a search engine. This Skill is written in Chinese because that is the language of the platform, its users, and the source material. If your AI can read Chinese, it can use this.

---

## What it does for you

| Where you're stuck | What it gives you |
|---|---|
| Nothing posted yet, agonizing over positioning | It refuses to do positioning analysis with you — it hands you a 10–20 post testing plan instead |
| Posting but getting no reach | Works backward from the recommendation mechanics: is it click-through, dwell time, or engagement that's failing |
| No idea what to write | 5 content types that reliably take off, plus three self-check questions to write against |
| Some traction, unclear next step | Publishing cadence and content mix by stage — 0–1K / 1K–5K / 5K–10K followers, down to specific percentages |
| Want to monetize but nobody's calling | The four-layer monetization structure, and why chasing revenue too early is what kills the account |

**Good fit:** personal-brand accounts in knowledge, career, AI, or design niches, from zero to 10K followers.
**Poor fit:** pure e-commerce accounts, storefronts, or batch account farming — the source author's experience does not cover those, and forcing the fit will mislead you.

---

## Installation

This Skill is **one folder and a few Markdown files**. No code, no dependencies, no network calls. Any AI that can read files can use it — only the installation step differs.

### Option 1: Let the AI install it (no command line needed)

If you use Claude Code, Codex, Cursor, or any other AI that can operate on files, **you don't need to type commands**. Copy the whole block below and hand it to your AI:

```
Please install this Skill for me: https://github.com/zdrjson/xhs-growth-skill

Work out where it belongs in my current environment:
- If this is Claude Code, clone the repo and copy the xhs-growth folder into ~/.claude/skills/
- If this is Codex, Cursor, Windsurf, or Cline, put the xhs-growth folder in the current
  project and add a line to the matching rules file (AGENTS.md / .cursor/rules/ /
  .windsurfrules / .clinerules):
  "When the conversation involves Xiaohongshu growth, cold start, follower growth, topic
  selection, viral content, or monetization, read xhs-growth/SKILL.md first, then follow
  its routing to the relevant references/ file."

When you're done, tell me how to confirm it worked and how I should phrase my questions.
```

Using it afterwards is the same idea — plain language, e.g. "I have 300 followers and 12 posts with no reach, what's wrong?"

### Option 2: Install it yourself

#### Claude Code (simplest)

```bash
git clone https://github.com/zdrjson/xhs-growth-skill.git
cp -r xhs-growth-skill/xhs-growth ~/.claude/skills/
```

**Restart Claude Code**, then just ask your question — it triggers on its own. To confirm it's installed, type `/` and look for `xhs-growth` in the skill list.

> Only want it in one project? Put `xhs-growth` in that project's `.claude/skills/` instead of `~/.claude/skills/`.

#### Claude desktop app / claude.ai

Both take an uploaded zip under **Skills** in settings:

```bash
git clone https://github.com/zdrjson/xhs-growth-skill.git
cd xhs-growth-skill && zip -r xhs-growth.zip xhs-growth
```

Then upload `xhs-growth.zip` under **Settings → Capabilities / Skills → Upload skill**.

#### Codex / Cursor / Windsurf / Cline and other coding agents

Most of these don't recognize the Skills format, but all of them read project instruction files. Put the folder in your project, then add one reference line to whichever rules file your tool uses:

```bash
git clone https://github.com/zdrjson/xhs-growth-skill.git
cp -r xhs-growth-skill/xhs-growth ./xhs-growth
```

| Tool | Rules file |
|---|---|
| Codex | `AGENTS.md` |
| Cursor | `.cursor/rules/xhs.mdc` |
| Windsurf | `.windsurfrules` |
| Cline / Roo | `.clinerules` |

The line is the same in all of them:

```
When the conversation involves Xiaohongshu growth, cold start, follower growth, topic
selection, viral content, or monetization, read xhs-growth/SKILL.md first, then follow
its routing to the relevant references/ file.
```

#### ChatGPT / Gemini / DeepSeek / Kimi and other chat AIs

Nothing to install. Two ways:

**① Upload the files** (recommended, works best)
Attach the `.md` files from `xhs-growth/references/` to the conversation, or add them to a ChatGPT Project, a Gemini Gem, or a NotebookLM source set. Then ask away.

**② Paste directly** (one-off use)
Open whichever file matches your situation (see the table below), copy all of it into the chat box, and end with:

```
The above is a Xiaohongshu growth methodology. My situation: ___ followers, ___ posts
published, my best-performing post was about ___. Give me specific advice based on the
methodology above.
```

One file at a time is enough — each is 4–6 KB and fits comfortably in any model's context.

---

## How to use it

No commands to memorize. All of these trigger it:

- "Why is my Xiaohongshu account getting no reach?"
- "Check this cover and title for me"
- "300 followers — what should I post this week?"
- "How many followers before brands start paying?"

**The more context you give, the more specific the answer.** Ideally state all four:

> current follower count · how many posts so far · which post performed best · what topic you can sustainably produce

Without those it can only give generic answers — SKILL.md makes this a hard requirement, so it will ask you for them.

---

## What's inside

```
xhs-growth/
├── SKILL.md                     Entry point: identifies your stage, loads only the 1–2 files needed
└── references/
    ├── 00-sources.md            Sources, author background, where these conclusions stop applying
    ├── 01-positioning.md        Positioning, persona, niche discipline, 8 cold-start mistakes
    ├── 02-cold-start.md         Recommendation mechanics, cover/title formulas, your first 10 posts
    ├── 03-viral-content.md      The virality formula, four-part post structure, 5 types that take off
    ├── 04-rhythm-0-10k.md       Content pipeline cadence, four-stage plan and content mix to 10K
    └── 05-monetization-ip.md    Four-layer monetization, how a personal IP actually forms, long-termism
```

Pick by where you're stuck (use this when pasting manually into a chat AI):

| Where you're stuck | File |
|---|---|
| Haven't started, stuck on positioning | `01-positioning.md` |
| Posting with no reach, weak titles/covers | `02-cold-start.md` |
| Don't know what to write, want a hit | `03-viral-content.md` |
| Have data, asking about cadence | `04-rhythm-0-10k.md` |
| Brand deals, rates, personal IP | `05-monetization-ip.md` |

---

## Positions it holds

These are drawn from the source material and hardcoded into the Skill. The AI will hold them:

- **Positioning is discovered by shipping, not decided in advance.** If you're agonizing over it, it won't analyze with you — it'll tell you to publish 10–20 posts.
- **Click-through is the first gate.** Cover and title outrank body copy. No click means the content never mattered.
- **Follower growth is downstream of trust, not of metrics.** 10K people who believe you beat 1M passersby.
- **Monetization is an outcome, not a starting point.** Chasing it early makes content pander and strips your distinctiveness.
- **The biggest threat to a new account isn't throttling — it's quitting after three posts.** Feedback is inherently delayed.

---

## Limits (please read)

The source author's experience is grounded in **knowledge / career / AI personal-IP** niches, with Silicon Valley and Harvard credentials behind her. Discount accordingly:

- "Sponsorship rate ≈ 1/10 of follower count" is that niche's going rate, **not a platform-wide standard**
- Her personal milestones (Harvard, the Spotify layoff, 200K followers) are case material, not a promised outcome
- Platform rules and distribution change; this material was compiled in August 2026

---

## Source and license

- Original articles: [@yanliudreamer's article list](https://x.com/yanliudreamer/articles) — five posts in the Xiaohongshu series
- The methodology belongs to the original author. This repository is a study compilation for non-commercial use and does not reproduce the article text.
- The compiled material is offered under MIT.

If this is useful to you, following [the original author](https://x.com/yanliudreamer) is worth more than starring this repo.
