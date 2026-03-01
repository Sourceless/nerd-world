---
layout: page
title: DM Guide
permalink: /dm-guide/
---

# DM Guide

Anyone can run a session in Nerd World. You don't need to be an expert. A small dungeon, a clear goal, and three hours is all it takes.

---

## Announcing a Session

Post in the **Facebook Messenger group** at least a week before. Include:

- **Date** — the third Saturday (or a rescheduled date if agreed)
- **Time** — when it starts and roughly when it ends
- **Where** — the location (or "same place as last time")
- **Hook** — one sentence about what the session involves. *"A merchant is paying for someone to investigate a disappearance near the Old Mill."* That's enough.

Players will reply to confirm. Aim for 3–5 players. More than 6 gets unwieldy.

---

## Preparing an Adventure

### Keep it short

A 3-hour session needs about **5–7 encounters** or meaningful scenes. That includes:
- 1–2 combat encounters
- 1–2 exploration or puzzle moments
- 1 social encounter (optional)
- A clear beginning, middle, and end

You don't need to script everything. Put interesting things in interesting places and let the players interact.

### A simple structure

1. **The hook** — why are the characters here?
2. **The journey** — something interesting on the way
3. **The place** — the dungeon, the ruin, the villain's lair
4. **The payoff** — treasure, information, or a resolution

### XP budget

Award XP based on challenge difficulty. A rough guide for a balanced session:

| Session Difficulty | Total XP Awarded |
|---|---|
| Easy (low danger) | 100–200 XP |
| Standard | 200–400 XP |
| Hard (real threat of death) | 400–600 XP |

Use the XP values in the *Monster Manual* for combat. Award bonus XP for creative problem-solving, good roleplay, or achieving the session goal.

---

## Posting a Session Report

This is the most important thing you do after a session. It keeps the shared history alive and lets players track their XP.

Session reports are posted by creating a file directly on GitHub — **no coding knowledge required**.

### Step 1: Go to the repository

Visit [github.com/Sourceless/nerd-world](https://github.com/Sourceless/nerd-world) and make sure you're logged into GitHub. (You'll need a free account, and the repo owner needs to have added you as a collaborator.)

### Step 2: Navigate to `_posts/`

Click the `_posts` folder in the file list.

### Step 3: Create a new file

Click **Add file → Create new file** (top right of the file list).

### Step 4: Name the file

Use this exact format:

```
YYYY-MM-DD-short-title.md
```

For example: `2026-04-19-old-mill-mystery.md`

The date must match the session date. The short title should be lowercase with hyphens, no spaces.

### Step 5: Paste the front matter

Copy this template and fill in your details:

```yaml
---
layout: post
title: "Your Session Title Here"
date: YYYY-MM-DD
dm: "Your Name"
players:
  - "Player One"
  - "Player Two"
  - "Player Three"
location: "Name of the in-world location"
xp_awarded: 300
tags:
  - dungeon
  - combat
---
```

**Front matter fields:**

| Field | What to put |
|---|---|
| `title` | The session title in quotes |
| `date` | The session date in YYYY-MM-DD format |
| `dm` | Your name in quotes |
| `players` | A YAML list of player names (one per line with `  - `) |
| `location` | Where the session took place in the world |
| `xp_awarded` | The total XP each player receives |
| `tags` | Keywords for the session (dungeon, combat, roleplay, exploration, etc.) |

### Step 6: Write the report

Below the front matter (after the second `---`), write your report in plain text. Aim for **under 500 words**. Cover:

- What the party set out to do
- The key moments (a fight, a discovery, a decision)
- The outcome — did they succeed? What changed in the world?
- Any notable NPCs or locations introduced

### Step 7: Commit the file

Scroll down to **Commit new file**. The default message is fine. Click **Commit new file** (the green button).

GitHub will automatically build and deploy the site. The report will appear on the [Sessions page]({{ '/sessions/' | relative_url }}) within a couple of minutes.

---

## Tips for Writing Good Reports

- **Write the same day.** Your memory fades fast. Even rough notes are better than nothing.
- **Name your NPCs.** "The innkeeper" is forgettable. "Aldric the innkeeper" becomes lore.
- **Note what changed.** Did they clear a dungeon? Kill a villain? Forge an alliance? This shapes what future DMs can reference.
- **Keep it under 500 words.** People will actually read it. A novel, they won't.
- **Be generous with credit.** Call out players who had great moments.

---

## After the Session

- Post the XP amount in Messenger so players can update their sheets
- Share any new locations or NPCs in the group — other DMs may want to build on them
- You're done! You ran a session. That's the whole deal.
