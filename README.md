# Stackhacks Git Lab

> A beginner-friendly Git workshop exercise by StackHacks

Welcome! This repo is used during our **Git Workshop** to practice real Git skills.  
By the end of this exercise, you'll have cloned a repo, made a branch, resolved a merge conflict, and opened a Pull Request — just like developers do every day.

---

## 🚀 The Exercise

Add your name (and a fun fact!) to `contributors.txt` by following the steps below.

---

## 📋 Step-by-Step Instructions

### 1. Clone the repo
```bash
git clone <repo-url>
cd stackhacks-git-lab
```

### 2. Create your branch
```bash
git checkout -b add-your-name
```

### 3. Edit `contributors.txt`
Open the file and add a new line in this format:
```
Your Name - Fun fact about yourself
```

### 4. Stage and commit your change
```bash
git add .
git commit -m "feat: add [your name] to contributors"
```

### 5. Push your branch
```bash
git push origin add-your-name
```

### 6. Open a Pull Request
Go to the repo on GitHub and open a Pull Request from your branch into `main`.  
A workshop host will review and merge it! 🎉

---

## ⚔️ Merge Conflicts

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

*Presented by [StackHacks]