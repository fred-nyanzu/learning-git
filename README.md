# Learning Git

My hands-on notes and exercises from learning Git and GitHub, collected in one place.

Each folder is a short exercise with the exact commands I used. You can follow along from start to finish in about 30 minutes.

## Exercises

| # | Exercise | What it covers |
|---|----------|----------------|
| 01 | [Git basics](01-git-basics/) | Creating a repo, staging, committing, pushing |
| 02 | [Branches and .gitignore](02-branches-and-gitignore/) | Working on branches, `main` and `master`, ignoring files |
| 03 | [First Python script](03-first-python-script/) | Adding code to a repo and fixing a bug in a commit |

## Prerequisites

- [Git](https://git-scm.com/downloads) installed (`git --version` to check)
- A free [GitHub](https://github.com) account
- [Python 3](https://www.python.org/downloads/) for exercise 03

## Quick start

```bash
git clone https://github.com/fred-nyanzu/learning-git.git
cd learning-git
```

Then open [01-git-basics](01-git-basics/) and work through the exercises in order.

## Cheat sheet

| Command | What it does |
|---------|--------------|
| `git init` | Start tracking a folder with Git |
| `git status` | See what has changed |
| `git add <file>` | Stage a file for the next commit |
| `git commit -m "message"` | Save a snapshot of staged changes |
| `git log --oneline` | List past commits |
| `git switch -c <branch>` | Create and move to a new branch |
| `git push` | Upload commits to GitHub |
| `git pull` | Download the latest commits |

## History

This repo combines my first three practice repos from 2021 (`classes`, `data_science_class` and `demo_tuto`) into one tidy place.
