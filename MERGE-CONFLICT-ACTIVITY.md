# Git Merge Conflict Activity

## Branches and conflicting edits

Both branches started from the same baseline commit (`b2d6d7d`):

- `branch-one` (`ccb02f1`) changed the status line to: `Project status: Built the portfolio with HTML and CSS.`
- `branch-two` (`daa5e09`) changed that same line to: `Project status: Created a CV website for employers.`

After merging `branch-one` into `main`, merging `branch-two` produced a content conflict in `merge-conflict-demo.txt`. Git marked the two competing versions with `<<<<<<<`, `=======`, and `>>>>>>>`.

## Resolution

The conflict was resolved on `main` by combining both changes into one sentence:

> Project status: Built the portfolio with HTML and CSS and created a CV website for employers.

The conflict markers were removed, and the final merge commit records both branch histories.

## Verification

The completed activity can be checked in the repository by viewing `main`, `branch-one`, and `branch-two`, then comparing their `merge-conflict-demo.txt` versions. The merge commit is the latest commit on `main`.

Commands used:

```text
git merge branch-one
git merge branch-two
git status
git add merge-conflict-demo.txt
git commit
git push origin main branch-one branch-two
```
