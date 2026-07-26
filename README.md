# LearnSalesforce
This contain code related ti salesforce learning
## Git Commands Cheat Sheet

### Setup (one-time)
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

### Starting a repo
git init                          # initialize a new repo
git clone <url>                   # copy an existing repo locally

### Daily basics
git status                        # see what's changed
git add <file>                    # stage a specific file
git add .                         # stage all changes
git commit -m "message"           # save a snapshot
git log                           # view commit history
git log --oneline                 # compact history view
git diff                          # see unstaged changes

### Branching
git branch                        # list branches
git checkout -b <branch-name>     # create + switch to new branch
git checkout <branch-name>        # switch branches
git branch -d <branch-name>       # delete local branch (safe)
git branch -D <branch-name>       # force delete local branch

### Syncing with remote
git remote add origin <url>       # link local repo to GitHub
git push -u origin <branch-name>  # push branch, set upstream (first time)
git push                          # push commits (after upstream is set)
git pull                          # fetch + merge latest changes
git fetch                         # download changes without merging

### Merging
git checkout main                 # switch to main
git merge <branch-name>           # merge branch into current one

### Undoing things
git checkout -- <file>            # discard uncommitted changes to a file
git reset --soft HEAD~1           # undo last commit, keep changes staged
git reset --hard HEAD~1           # undo last commit, discard changes (careful!)
git revert <commit-hash>          # safely undo a specific commit (new commit)

### Inspecting
git diff <branch1> <branch2>      # compare two branches
git show <commit-hash>            # view details of a specific commit
git blame <file>                  # see who changed each line and when

### Stashing (save work temporarily without committing)
git stash                         # shelve current changes
git stash pop                     # reapply last stashed changes
git stash list                    # see all stashes