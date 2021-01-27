# Git Cheetsheets


## Create branch
Create a branch from the branch you are working on:
`git checkout -b <your branch name>`

Create a branch from a tag:
`git checkout -b <your branch name> <tag>`

## Commit

`git add .`
`git commit -m 'Commit message'`

## Trigger Build with empty commit
`git commit --allow-empty -m "Trigger Build"`

## Push
Push your changes to the branch you are working on as shown below:

`git push origin <branch-name>`


## Upstream
After fork, To create a link to the original repository, copy and paste the following command into your terminal:
`git remote add upstream <upstream address>`
You can use `git pull upstream master` to confirm if there has been any change at the moment (from when you forked the repository to now).



## Rebase
First fetch the new master from the upstream repository, then rebase your work branch on that:
`git fetch origin            # Updates origin/master`
`git rebase origin/master    # Rebases current branch onto origin/master`


## Rename commits
Use interactive rebase to delete/rename old commits
`git rebase -i HEAD~x`
when `x` is the number of history commits you want to work on.
Then change each one of the commits in the editor and save, late  we need to resolve conflicts.