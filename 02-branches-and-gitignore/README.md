# 02 · Branches and .gitignore

**Goal:** make changes safely on a branch, merge them back, and keep unwanted files out of the repo.

## Branches

**1. Create a branch and switch to it**

```bash
git switch -c day-2-practice
```

**2. Make a change and commit it**

```bash
echo "Day 2 notes" > day2.md
git add day2.md
git commit -m "Add day 2 notes"
```

**3. Go back to `main` and merge**

```bash
git switch main
git merge day-2-practice
git branch -d day-2-practice   # delete the branch once it is merged
```

> **Lesson learned:** older repos used `master` as the default branch, and GitHub now uses `main`.
> My first attempt ended up with work split across both. Pick one branch as the default
> (`git branch -M main`) and merge everything into it.

## .gitignore

A `.gitignore` file lists files Git should never track, such as temporary files, secrets or build output.

**1. Create the file**

```bash
cat > .gitignore << 'EOF'
# Python
__pycache__/
*.pyc

# Editors and OS
.vscode/
.DS_Store
Thumbs.db

# Secrets
.env
EOF
```

**2. Check that it works**

```bash
touch .env
git status   # .env does not appear
```

**3. Commit it**

```bash
git add .gitignore
git commit -m "Add .gitignore"
```

## What I learned

- Branches let me try things without breaking `main`.
- Ignore files *before* committing them. Once tracked, they need `git rm --cached <file>`.
- Never commit passwords or API keys, even in a practice repo.

**Previous:** [01 · Git basics](../01-git-basics/) · **Next:** [03 · First Python script](../03-first-python-script/)
