# GitPath — Interactive Git Learning Platform

> Master Git through real production scenarios, structured tracks, and a live terminal — all inside a single HTML file.

![GitPath](https://img.shields.io/badge/GitPath-v2.0-00e87a?style=for-the-badge&logo=git&logoColor=white)
![HTML](https://img.shields.io/badge/HTML-Single%20File-orange?style=for-the-badge&logo=html5&logoColor=white)
![No Dependencies](https://img.shields.io/badge/Dependencies-None-blue?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-purple?style=for-the-badge)

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Getting Started](#-getting-started)
- [Learning Tracks](#-learning-tracks)
- [Production Scenarios](#-production-scenarios)
- [Supported Git Commands](#-supported-git-commands)
- [Progress & XP System](#-progress--xp-system)
- [Project Structure](#-project-structure)
- [Tech Stack](#-tech-stack)
- [Screenshots](#-screenshots)
- [Contributing](#-contributing)
- [Author](#-author)
- [License](#-license)

---

## 🚀 Overview

**GitPath** is a fully self-contained, browser-based Git learning platform built for DevOps engineers, developers, and anyone who wants to move beyond `git add .` and `git commit`. It combines:

- A **live interactive terminal** that simulates real git commands
- A **visual branch graph** rendered on canvas in real time
- **28 guided lessons** across 7 structured tracks from beginner to pro
- **8 production-grade scenarios** including 2AM hotfixes, security incidents, and GitFlow releases
- A **persistent XP and progress system** saved in your browser

No server. No install. No account. Just open `index.html` and start learning.

---

## ✨ Features

### 🖥️ Interactive Terminal
- Simulates a real git environment — type commands and see authentic output
- **20+ git commands** supported with proper error handling
- Arrow-key **command history** navigation
- **Tab autocomplete** for common commands
- Quick-chip shortcuts for frequently used commands

### 📊 Live Branch Graph
- Canvas-rendered commit tree that updates with every command
- Merge commits shown as diamonds with dashed parent lines
- Branch label pills float above each tip commit
- Click any node to auto-fill a `git checkout <hash>` command
- Pan and zoom support

### 🗺️ Structured Learning Path
- 7 tracks from beginner to pro-level DevOps
- Each lesson has a **real-world story** (not just dry command docs)
- Step-by-step task tracker with live completion detection
- Hint system — reveals the next command if you're stuck
- Auto-advances to the next lesson on completion

### 🏆 Progress & XP System
- Every lesson awards XP (20–120 points based on complexity)
- Progress persists via `localStorage` — survives browser restarts
- Dashboard shows: lessons completed, scenarios done, total XP, and daily streak 🔥
- Track-level progress bars on the landing page
- Lesson pills update to green ✓ when completed

### 🔒 Privacy First
- **Zero data leaves your machine** — everything runs client-side
- No analytics, no tracking, no accounts
- Progress stored in your browser's `localStorage` only

---

## 🏁 Getting Started

### Option 1 — Open directly (simplest)

```bash
# Clone the repo
git clone https://github.com/surya-4220/git-simulator.git

# Navigate into the folder
cd gitpath

# Open in your browser
open index.html          # macOS
xdg-open index.html      # Linux
start index.html         # Windows
```

No build step. No `npm install`. No server needed.

### Option 2 — Serve locally (optional, for Live Reload)

```bash
# Using Python (comes pre-installed on most systems)
python3 -m http.server 8080

# Then open in browser
open http://localhost:8080
```

### Option 3 — VS Code Live Server

Install the [Live Server extension](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer), right-click `index.html`, and select **Open with Live Server**.

---

## 📚 Learning Tracks

GitPath is organized into **7 tracks** with **28 lessons** totalling **1,710 XP**.

---

### 🌱 Track 1 — Git Basics `Beginner`

Foundation concepts every developer must know.

| Lesson | XP | Description |
|---|---|---|
| Your First Commit | 30 | `git init`, `git add`, `git commit`, `git log` — the full first-time workflow |
| Configure Git Identity | 20 | Set `user.name` and `user.email` — why it matters for CI and blame |
| Staging Area Deep Dive | 40 | Stage individual files, preview diffs, craft logical commits |

---

### 🌿 Track 2 — Branching & Merging `Beginner`

Parallel development, merging strategies, and conflict resolution.

| Lesson | XP | Description |
|---|---|---|
| Feature Branch Workflow | 50 | The golden rule: never commit to main — branch, commit, merge |
| Checkout vs Switch | 25 | Classic `git checkout` vs modern `git switch` — when to use each |
| Merge Strategies | 60 | Fast-forward vs 3-way merge — how diverged histories get joined |
| Resolving Merge Conflicts | 80 | Two engineers, one file — identify, resolve, and commit |

---

### 🌐 Track 3 — Remote Collaboration `Intermediate`

Working with teams through push, pull, fetch, and pull requests.

| Lesson | XP | Description |
|---|---|---|
| Connecting to Remote | 40 | `git remote add`, push, fetch, pull — connecting local to GitHub |
| Pull Request Workflow | 60 | Feature branch → push → PR → merge → cleanup |
| Fetch vs Pull vs Rebase Pull | 45 | Three sync strategies and when each one is the right call |

---

### ⏳ Track 4 — Rewriting History `Intermediate`

Rebase, cherry-pick, amend, squash — tools senior engineers use daily.

| Lesson | XP | Description |
|---|---|---|
| Rebase for Clean History | 70 | Replay commits on top of latest main for linear history |
| Interactive Rebase — Squash | 90 | Collapse WIP commits into one clean commit before PR review |
| Cherry-Pick | 65 | Apply a single commit from develop to production without merging everything |
| Amend & Revert | 55 | `--amend` for private fixes, `revert` for safe shared-branch undo |

---

### 🚀 Track 5 — Production Workflows `Advanced`

Real incident response and release processes used at scale.

| Lesson | XP | Description |
|---|---|---|
| 🔥 Hotfix Deployment | 100 | 2AM production outage — branch from main, fix, deploy to main AND develop |
| GitFlow Release Process | 120 | Full sprint cycle: feature → develop → release → main → tag |
| Security: Leaked Credentials | 110 | AWS keys committed to main — revert, rotate, document the incident |
| Release Tagging & Versioning | 70 | Lightweight vs annotated tags, semantic versioning, CI/CD triggers |

---

### ⚡ Track 6 — Advanced Git `Advanced`

Power-user techniques that save hours and prevent disasters.

| Lesson | XP | Description |
|---|---|---|
| Binary Search with Bisect | 100 | Find which commit introduced a regression in O(log n) steps |
| Recovering Lost Commits | 85 | `git reflog` — nothing is truly lost for 90 days |
| Advanced Stash Techniques | 60 | Named stashes, context switching mid-feature, stash list management |
| Multiple Worktrees | 90 | Review a PR and work on a feature simultaneously — zero stashing |

---

### 🔄 Track 7 — CI/CD & DevOps Git `Pro`

How Git integrates with pipelines, monorepos, and automation at enterprise scale.

| Lesson | XP | Description |
|---|---|---|
| Conventional Commits | 50 | `feat:`, `fix:`, `chore:` — the standard that powers auto-changelog and semver |
| Monorepo Git Strategy | 100 | Scoped commits, per-service CI triggers, breaking change notation |
| Branch Protection Strategy | 80 | PRs, CI gates, approval rules — the full team workflow |

---

## 🎯 Production Scenarios

Eight standalone challenges based on real incidents and workflows. Each drops you into a story with full context before you start typing.

| # | Scenario | Difficulty | Tags |
|---|---|---|---|
| 🔥 | **2AM Hotfix Deployment** | Critical | `gitflow` `prod` `incident` |
| 🚢 | **GitFlow Release Cycle** | Advanced | `release` `semver` `gitflow` |
| 🔐 | **Leaked Credentials Response** | Critical | `security` `revert` `compliance` |
| ⚔️ | **Merge Conflict Resolution** | Intermediate | `conflict` `merge` `team` |
| 🏷️ | **Semantic Release Tagging** | Intermediate | `semver` `tags` `ci-cd` |
| ✂️ | **Squash Before PR Review** | Advanced | `rebase` `pr-hygiene` `history` |
| 📋 | **Auto-changelog Pipeline** | Intermediate | `ci-cd` `semver` `automation` |
| 🧲 | **Recover Lost Commits** | Advanced | `recovery` `reflog` `emergency` |

---

## 💻 Supported Git Commands

GitPath simulates the following commands with realistic output and state tracking:

| Category | Commands |
|---|---|
| **Init & Config** | `git init`, `git config` |
| **Staging** | `git add`, `git restore`, `git status`, `git diff` |
| **Commits** | `git commit`, `git commit --amend` |
| **Branching** | `git branch`, `git checkout`, `git switch` |
| **Merging** | `git merge` |
| **Rebase** | `git rebase` |
| **Remote** | `git remote`, `git fetch`, `git pull`, `git push` |
| **Undo** | `git reset` (soft/mixed/hard), `git revert` |
| **History** | `git log`, `git log --oneline`, `git log --graph` |
| **Stash** | `git stash push`, `git stash pop`, `git stash list`, `git stash drop` |
| **Advanced** | `git cherry-pick`, `git tag`, `git bisect`, `git worktree` |
| **Help** | `git help` |

> **Note:** This is a simulation. Commands run against an in-memory state engine, not a real filesystem. The output and behaviour mirror real git closely for learning purposes.

---

## 🏆 Progress & XP System

| Metric | Details |
|---|---|
| **Total Lessons** | 28 across 7 tracks |
| **Total XP Available** | 1,710 XP |
| **Scenario Count** | 8 production challenges |
| **Persistence** | `localStorage` — survives page reloads |
| **Streak** | Increments each calendar day you complete a lesson |
| **Reset** | Footer → "Reset Progress" button |

XP is awarded per lesson on completion. The dashboard on the landing page shows live progress bars for lessons, scenarios, XP, and daily streak.

---

## 🗂️ Project Structure

```
gitpath/
│
├── index.html          # The entire application — HTML + CSS + JS in one file
└── README.md           # This file
```

GitPath is intentionally a **single-file application**. This makes it:
- Trivial to share (send one file)
- Hostable anywhere (GitHub Pages, S3, Netlify, local drive)
- Easy to fork and customise — all logic is in one place

---

## 🛠️ Tech Stack

| Layer | Technology | Why |
|---|---|---|
| **UI Framework** | Vanilla HTML/CSS/JS | Zero dependencies, maximum portability |
| **Styling** | CSS custom properties + Grid/Flex | Dark theme, responsive, no build step |
| **Graph** | HTML5 Canvas API | Real-time branch visualization |
| **Fonts** | Google Fonts (Clash Display, DM Mono, DM Sans) | Loaded via CDN |
| **Persistence** | `localStorage` | Client-side only, no server needed |
| **Git Engine** | Custom JS state machine | Simulates commits, branches, merges, rebase |

No React. No Vue. No Webpack. No `node_modules`. No build pipeline.

---

## 🧩 Extending GitPath

Want to add your own lessons or modules? The data structure is straightforward:

```javascript
// Add a new module inside the MODULES array
{
  id: 'my-module',
  title: 'My Custom Track',
  icon: '🎯',
  diff: 'inter',           // begin | inter | adv | pro
  desc: 'Short description shown on landing page',
  lessons: [
    {
      id: 'my-lesson',
      title: 'My First Lesson',
      xp: 60,
      breadcrumb: 'My Module → My First Lesson',
      story: `<strong>Context here.</strong> Explain the real-world situation.
               Use <code>inline code</code> for commands.`,
      objectives: [
        {
          cmd: 'git commit -m "example"',
          desc: 'What this step achieves',
          hint: 'Helpful tip shown when user clicks Hint'
        },
        // add more steps...
      ],
      setup: () => {
        resetGit();
        addFile('src/example.js');
        // optional: pre-create branches
        // git.branches.develop = null;
      }
    }
  ]
}
```

Add a corresponding entry to `PROD_SCENARIOS` if you want the lesson to also appear as a scenario card on the landing page.

---

## 📸 Screenshots

### Landing Page — Progress Dashboard
The landing page shows a live progress dashboard with XP, lesson count, scenario count, and daily streak. Track cards display per-lesson completion status with colour-coded dots and progress bars.

### Learning Path Tracks
Each track card shows:
- Difficulty badge (Beginner / Intermediate / Advanced / Pro)
- XP earned vs total available
- Progress bar (green = complete, blue = in progress)
- Individual lesson pills with ✓ when done

### Production Scenario Cards
Scenario cards show a "✓ Completed" badge and green border after you finish them.

### App View — Terminal + Graph
Split layout: left sidebar for track navigation, center terminal with live git engine, right panel for objectives/graph/state/cheatsheet.

---

## 🤝 Contributing

Contributions are welcome. Here are the most useful ways to help:

**Add new lessons**
Follow the data structure above and open a PR. Good targets: `git bisect` deep dive, `git rerere`, sparse checkouts, Git LFS basics.

**Improve the git engine**
The command parser is in the `exec()` function. Additional flag support (e.g. `git log --author`, `git stash branch`) is always useful.

**Bug reports**
Open an issue with the command you ran and what you expected vs what happened.

**Design improvements**
CSS-only changes are straightforward — everything is in the `<style>` block at the top of `index.html`.

---

## 👤 Author

**Surya Teja Bonala**
DevOps Engineer · 9 years IT experience · Hyderabad, India

- 📧 [suryateja.bonala@gmail.com](mailto:suryateja.bonala@gmail.com)
- 💼 [LinkedIn](https://www.linkedin.com/in/suryateja-bonala-2a9097216)
- 🐙 [GitHub](https://github.com/surya-4220)

Built as part of a hands-on DevOps portfolio project — practicing the git workflows used daily in production environments.

---

## 📄 License

MIT License — free to use, modify, and distribute.

```
MIT License

Copyright (c) 2025 Surya Teja Bonala

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

<div align="center">
  <sub>Built with 💚 · No frameworks harmed in the making of this project</sub>
</div>
