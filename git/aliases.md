# Git Aliases

Useful aliases I keep in my `.gitconfig`.

```ini
[alias]
    st = status -sb
    co = checkout
    cb = checkout -b
    cm = commit -m
    ca = commit --amend --no-edit
    lg = log --oneline --graph --decorate -20
    df = diff --stat
    undo = reset --soft HEAD~1
    wip = !git add -A && git commit -m "wip"
    nuke = !git clean -fd && git checkout -- .
    branches = branch --sort=-committerdate --format='%(committerdate:relative)%09%(refname:short)'
```

## Quick setup

```bash
# paste into terminal to apply all at once
git config --global alias.st "status -sb"
git config --global alias.co "checkout"
git config --global alias.cb "checkout -b"
git config --global alias.cm "commit -m"
git config --global alias.ca "commit --amend --no-edit"
git config --global alias.lg "log --oneline --graph --decorate -20"
git config --global alias.df "diff --stat"
git config --global alias.undo "reset --soft HEAD~1"
```
