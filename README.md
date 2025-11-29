# Quick Setup
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

git add
git add file.txt            # stage one file
git add .                   # stage all changed files in current dir

git commit
git commit -m "short message describing change"
If you forgot to stage, you can do:
git commit -am "save: edited tracked files"   # stages & commits tracked files only


git push
git push                 # pushes current branch to its upstream (if set)
git push -u origin feat  # push branch 'feat' and set upstream

# Branching & remotes
git clone git@github.com:org/project.git mycopy

git branch               # list local branches
git branch -a            # list local + remote-tracking branches
git switch -c feat/new   # create + switch to new branch (modern)
git switch feat/new      # switch to existing branch
old-style:
git checkout -b feat/new


git fetch

Download commits and update origin/* remote-tracking refs. Does not change local branches.

git fetch
git fetch origin
git fetch -p 

# Merging -
Integrate a branch into your current branch.
git switch main
git merge origin/main 

# Merge Conflicts
git switch main
git fetch origin          # get latest remote commits

git merge origin/main     # or if pulling:
git pull

Open the conflicted file(s) and look for markers
Then git add <file name>
git commit 
git push

