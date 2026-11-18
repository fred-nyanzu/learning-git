# 03 · First Python script

**Goal:** add real code to a repo, find a bug, and fix it in a follow-up commit.

## Run it

```bash
cd 03-first-python-script
python hello.py
```

Output:

```text
Hello, world!
```

## The bug I fixed

My first version had a missing quote:

```python
print(Hello word")
```

Python stopped with `SyntaxError: unterminated string literal`. The fix was to quote both ends of the text (and fix the typo):

```python
print("Hello, world!")
```

Committing the fix separately keeps the history readable:

```bash
git add hello.py
git commit -m "Fix syntax error in hello.py"
```

## What I learned

- Run code before committing it.
- Error messages point to the line to look at.
- Small, focused commits make it easy to see what changed and why.

**Previous:** [02 · Branches and .gitignore](../02-branches-and-gitignore/) · [Back to start](../)
