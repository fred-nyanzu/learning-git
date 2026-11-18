# 01 · Git basics

**Goal:** create a repository, save some changes, and put them on GitHub.

## Steps

**1. Tell Git who you are** (one time only)

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

**2. Create a folder and start tracking it**

```bash
mkdir my-first-repo
cd my-first-repo
git init
```

**3. Add a file**

```bash
echo "These are my practice notes" > notes.md
git status        # notes.md shows as untracked
```

**4. Stage and commit it**

```bash
git add notes.md
git commit -m "Add practice notes"
git log --oneline  # your commit is listed
```

**5. Edit the file and commit again**

```bash
echo "Second line" >> notes.md
git diff           # shows exactly what changed
git commit -am "Update notes"
```

**6. Push to GitHub**

Create an empty repo on GitHub first (no README), then:

```bash
git remote add origin https://github.com/<your-username>/my-first-repo.git
git branch -M main
git push -u origin main
```

## What I learned

- A commit is a saved snapshot. `git add` picks *what* goes in it.
- `git status` and `git diff` show where you are before you commit.
- `git push` only uploads commits, not unsaved or unstaged changes.

**Next:** [02 · Branches and .gitignore](../02-branches-and-gitignore/)
