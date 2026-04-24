# StackHacks Git Lab


> A beginner-friendly Git workshop exercise by StackHacks

Welcome! This repo is used during our **Git Workshop** to practice real Git skills in groups.  
By the end of this exercise, you'll have:
* cloned a repo,
* made a branch, 
* used `git stash`, 
* survived a merge conflict, and 
* opened a Pull Request (PR) 

— just like developers do every day.

NOTE: Only the host is allowed to edit this file! 
---

## 🚀 The Exercise — "The Living Story" 📖

Work in **groups on one laptop**. Groups are considered either pairs or trios (individual would be a last resort). Together you'll add a line to a shared story file — the host will make two secret edits to line 1 along the way, guaranteeing a merge conflict for everyone in Phase 4. You'll also practice `git stash` in a realistic scenario.

> 💡 Take turns! One person drives (types the commands), the other(s) navigate (read the instructions). Swap roles at each phase.

---

## 📋 Step-by-Step Instructions

### Phase 1 — Clone & Branch 
```bash
git clone <repo-url>
cd stackhacks-git-lab
git checkout -b group-[your-number]-branch
```

### Phase 2a — Write Your Line
Open `story.txt` and add **one new line** to your assigned section. Be creative!

⚠️ **Stop here — do NOT stage or commit yet. Wait for the host's signal.**

### Phase 3 — The Stash Challenge
The host will announce an urgent update to `main`. You need to pull it — but you have unsaved changes in your working directory!

You can't pull with uncommitted changes. Figure out how to temporarily save your work, pull the update, then restore it.

> 💡 Check the cheat sheet if you're stuck!

```bash
git stash
git pull origin main
git stash pop
```

### Phase 2b — Commit & Push
Now that you've pulled the latest changes, finish your work:
```bash
git add .
git commit -m "feat: add group [number] story line"
git push origin group-[your-number]-branch
```

### Phase 4 — Merge Conflict
Open your PR on GitHub. The host will merge everyone's PRs into `main`.

Now pull the latest changes:
```bash
git checkout main
git pull
git checkout group-[your-number]-branch
git merge main
```

The host has made a second edit to line 1 since you last pulled — so **everyone will get a merge conflict** when they merge `main` into their branch. Don't panic — work through it together:

1. Open `story.txt` — Git marks the conflict like this:
```
<<<<<<< HEAD
Once upon a time, there was an EPIC hackathon...
=======
Once upon a time, there was an EPIC hackathon that changed everything...
>>>>>>> main
```
2. Keep the version you want and **delete the markers**
3. Then finish the resolution:
```bash
git add .
git commit -m "fix: resolve merge conflict on opening line"
git push origin group-[your-number]-branch
```

### Phase 5 — Final PR & Read the Story 
Open your final PR on GitHub. The host will merge them all and everyone does a final pull:
```bash
git checkout main
git pull
cat story.txt
```
Read the completed story together — the more chaotic the better! 🎉

---

## ⚔️ Merge Conflict Cheat Sheet

If you run into a merge conflict, don't panic! Here's what to do:

1. Open the file — Git marks conflicts like this:
```
<<<<<<< HEAD
Your version
=======
Someone else's version
>>>>>>> their-branch
```
2. Keep the code you want and **delete the markers**
3. Then run:
```bash
git add .
git commit
```

---

## 📖 Quick Command Cheat Sheet

### ⚙️ Setup
| Command | What it does |
|---|---|
| `git config --global user.name "Your Name"` | Set your Git username |
| `git config --global user.email "you@email.com"` | Set your Git email |
| `git init` | Initialize a new local repo |
| `git clone <url>` | Copy a remote repo to your machine |

### 📁 Everyday Commands
| Command | What it does |
|---|---|
| `git status` | See what's changed or staged |
| `git add .` | Stage all changed files |
| `git commit -m "msg"` | Save a snapshot with a message |
| `git push` | Upload your commits to the remote |
| `git pull` | Download and merge remote changes |
| `git log --oneline` | View a compact commit history |

### 🌿 Branching
| Command | What it does |
|---|---|
| `git branch <branch-name>` | Create a new branch |
| `git checkout <branch-name>` | Switch to an existing branch |
| `git checkout -b <branch-name>` | Create and switch to a new branch |
| `git branch -d <branch-name>` | Delete a local branch |

### 🔀 Merging
| Command | What it does |
|---|---|
| `git checkout main` | Switch to the main branch |
| `git merge <branch-name>` | Merge a branch into your current branch |

### 🗄️ Stashing
| Command | What it does |
|---|---|
| `git stash` | Temporarily save uncommitted changes and clean your working directory |
| `git stash pop` | Restore your most recently stashed changes |
| `git stash list` | View all saved stashes |
| `git stash drop` | Delete the most recent stash |

> 💡 **Tip:** Use `git stash` when you need to quickly switch branches but aren't ready to commit your current work yet!

> 💡 **Tip:** Run `git status` often — it tells you exactly what to do next!

---

## ✅ Commit Message Format

We follow this convention:
```
<type>(<scope>): <short summary>
```
**Examples:**
- `feat: add Jane Doe to contributors`
- `fix: correct typo in contributor entry`
- `docs: update README instructions`

---

## 🙌 Contributors

See [contributors.txt](./contributors.txt) for everyone who has completed the exercise!

---

*Presented by [StackHacks](https://github.com) — thanks for coming!*