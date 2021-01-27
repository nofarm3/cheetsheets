# Git Cheetsheets

## Rebase
First fetch the new master from the upstream repository, then rebase your work branch on that:
`git fetch origin            # Updates origin/master`
`git rebase origin/master    # Rebases current branch onto origin/master`



## Rename commits
Use interactive rebase to delete/rename old commits
`git rebase -i HEAD~x`
when `x` is the number of history commits you want to work on.
Then change each one of the commits in the editor and save, late  we need to resolve conflicts.