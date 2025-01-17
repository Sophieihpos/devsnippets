---
title: Git
description: Git Dev Snippets
extends: _layouts.documentation
section: content
---

# Git

### Create a Directory
```bash
mkdir <folder-name>
```

### Create Empty File
```bash
touch <file-name-with-type>
```

### Initialize Git

```bash
git init
```

### Show the working tree status

Check the status of the repository

```bash
git status
```

### Add file contents to the index

Prepare the content staged for the next commit.

```bash
git add .
```

### Record changes to the repository

Use the given <msg> as the commit message. If multiple -m options are given, their values are concatenated as separate paragraphs.

```bash
git commit -m"your commit message"
```

--- 

## Repositories

### Create a new repository

Create a new repository on the command line.

```bash
echo "# devsnippets" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/rickwest/devsnippets.git
git push -u origin master
```

### Push an existing repository

Push an existing repository to a remote location from the command line.

```bash
git remote add origin https://github.com/rickwest/devsnippets.git
git push -u origin master
```

---

## Branches

### List branches

List existing branches. Current branch will be highlighted with an asterisk.

```bash
git branch --list
```

List existing remote branches.

```bash
git branch -r
# or
git branch --remote
```

List all existing branches (local and remote).

```bash
git branch -a
# or
git branch --all
```

### Compare branches

Lists the differences between two different branches.

```bash
git diff branchname1 branchname2
```

### Create a new branch

Creates a new branch and switches to it

```bash
git checkout -b branchname
```

### Switch to a branch

Changes to a branch based on name

```bash
git checkout branchname
```

### Merge a branch

To merge a branch into another, you need to do the following

1. **Checkout** the branch/master you wish to merge _into_
2. Merge the required branch into this one

```bash
git checkout branchname
git merge my-new-function
```

### Delete a branch

Deletes a branch thats no longer required (eg after a merge)

```bash
git branch -d branchname 
```

---

## Stashing

### Stash

When you want to switch branches but aren't ready to commit your changes, you can stash them away.

```bash
git stash
```

### Stash List

To see a list of the stashes you've stored.

```bash
git stash list
```
### Apply Stash 

To reapply your last stash

```bash
git stash apply
```

To apply an older stash, use your <code>git stash list</code> and append the stash number you want to apply to <code>git stash apply</code>.

```bash
git stash apply stash@{1}
```