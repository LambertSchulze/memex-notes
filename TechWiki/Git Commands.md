---
category: list
tags:
  - Git
  - KeyboardShortcuts
  - List
created: 2024-11-20
---
## Staging

`git add -p`
Select every chunk of changes if you want to stage them

`git add .`
Stage all changes

`git restore .`
Unstage all changes


## Commiting

`git commit -m "If applied, this commit will ..."`
Create a new commit with message

`git commit --amend`
Add changes to the last commit

`git commit --amend -m "Fix typo/wording in commit message"`
Change message of last commit

`git revert <commit-hash>`
Undo a commit

`git reset @^`
Undo last commit (changes in working directory)

`git reset --soft @^`
Undo last commit (changes staged)

`git reset --hard @^`
Undo last commit (changes deleted)

`git commit --fixup <commit-hash>`
Add fixes to a commit.
<strong>Be careful to not merge fixup commits to the main branch.</strong>
This can mess up CI Pipelines.

To squash fixup commits, use `git rebase -i --autosquash`.

`git commit -n` or `--no-verify`
Skips running the hooks

`git commit --allow-empty`
Allows the creation of a commit without file changes.
This is usually a bad idea.

## Log Information

`git status`
Show changed files in working directory and staging area

`git diff`
Shows all changes between the working directory and HEAD

`git log --graph`
Show history of commits with branch tree view

`git reflog`
Show history of states the local HEAD was in.
With this you can go back to the past and back again.
