# Question 1 — Git Basic Operations

This folder contains a real Git repository (including the hidden .git directory) with three commits. Open the extracted folder in VS Code and use its terminal. Git must be installed.

## Inspect the repository

```bash
git status
git log --oneline
```

## Undo the third commit using revert

```bash
git revert --no-edit HEAD
git log --oneline
```

This creates a fourth commit that removes the footer.

## Undo the revert using reset

```bash
git reset --hard HEAD~1
git log --oneline
```

This restores the original three commits and footer. Warning: hard reset discards uncommitted changes. Use only in this practice repository before pushing.

## Push to GitHub

Create an empty repository on GitHub (do not initialize with README). Replace YOUR_USERNAME with your GitHub username.

```bash
git remote add origin https://github.com/YOUR_USERNAME/git-basic-operations.git
git remote -v
git push -u origin main
```

Authenticate when prompted. No remote is configured in this ZIP, and no push has been performed.

## Recreate the three commits from scratch (optional)

In a separate empty folder, run `git init -b main`. Create index.html with a heading, run `git add index.html` and `git commit -m "Create index.html"`. Add a paragraph and repeat add/commit with message `Add introduction paragraph`. Add a footer and repeat with message `Add footer`. Configure your Git name/email if Git asks.
