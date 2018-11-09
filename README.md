# Git usage cheatsheet
## Basics
* **Install Git:<br>**
conda install git
* **Check Git version:<br>**
git --version
* **Check Git configuration:<br>**
git config --list
* **Check Git command help:<br>**
git config --help
* **Initiate a new git under the same folder<br>**
git init
* **Config the username and email for first usage:<br>**
git config --global user.name 'Kai Hu' <br>
git config --global user.email 'hukai916@gmail.com'
* **Display changes made:<br>**
git diff
* **Add to the staging/index for future commit:<br>**
git add
* **Remove from staging area:<br>**
git reset
* **Submit to local repository:<br>**
git commit
* **Add file to staging status:<br>**
git add
* **Remove file from staging status:<br>**
git rm --cached <file>
  * Without --cached flag, files will also be removed from working directory.
* **Unstage file:<br>**
git reset <filename>
* **Add all files to staging status:<br>**
git add .<br>

When you change staged files, and do git status to check their status, they will be listed as changed too.

## Branching
* **Create new branch:<br>**
git branch branch_name <br>
git brand -a
  * List all branches including remote
* **Switch branches:<br>**
git checkout branch_name
* **Merge branches:<br>**
git merge branch_name

If you are working on your own project, you don't even need a branch. You must commit or stash your changes before you can switch branches.

## Remote repository basics
* **Get a list of remote repositories:<br>**
git remote
* **Submit local branch to remote repository:<br>**
git remote add origin https://github.com/hukai916/Git_cheat_sheet.git
  * The "origin" is the assigned name for remote repository, can be changed.
* **Submit to remote repository: (use SH key to ignore user info input)<br>**
git push -u origin master https://github.com/hukai916/Git_cheat_sheet.git <br>
  * origin is the name of the remote repository while master is the branch name
  * usually push to another remote branch for further adjustment before merging with remote master
git push
* **Get local copy of remote repository:<br>**
git clone <url> <where to clone>
* **Retrieve the latest updates from remote repository:<br>**
git pull
  * Useful when working as a team, before git push local changes to master, git pull to retrieve other's update

To intentionally un-track sensitive files that contain non-codes related information, put their names into .gitignore file.

A typical workflow: git branch branch1 -> git checkout branch1 (working on branch1) -> git add -> git commit -> git push -u origin branch1 -> git checkout master -> git pull origin master -> git merge branch1 -> git push master

## Fixing common mistakes
* **Delete unwanted changes to file:<br>**
git checkout filename.txt
  * must be done before git add
* **Modify commit message:<br>**
git commit --amend -m "message to change"
  * this would change git history, may cause trouble if other people already pulled the changes
* **Move commit to another branch:<br>**
git log<br>
git cherry-pick commit-hash-from-other-branch
git reset --soft commit-hash-to-return-to
  * git log to get the unique hash for commit to move, cherry-pick to move that commit to current branch
  * cherry-pick won't delete old commit, to delete, use git reset commit-hash-to-return-to
  * git reset --soft: tracked file still in staging
  * git reset --mix: default, tracked file still in working directory
  * git reset --hard: be careful, will match the status of tracked files back to the state they were. To clean untracked files: git clean -df
  * git clean -df: really handy, just clean all untracked files.
* **To undo hard reset<br>**
git reflog <br>
git checkout command-hash
git branch backup
  * reflog is to pull out the command-hash
  * checkout command-hash will only create a detached headed file will be deleted later on anyway
  * to secure, create another branch
* **Undo commits without change log history:<br>**
git revert commit-hash
  * will create another commit that undo specified commit without changing history
