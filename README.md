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

If you are working on your own project, you don't even need a branch.

## Remote repository basics
* **Get a list of remote repositories:<br>**
git remote
* **Submit local branch to remote repository:<br>**
git remote add origin https://github.com/hukai916/Git_cheat_sheet.git
  * The "origin" is the assigned name for remote repository, can be changed.
* **Submit to remote repository: (use SH key to ignore user info input)<br>**
git push -u origin master https://github.com/hukai916/Git_cheat_sheet.git <br>
git push
* **Get local copy of remote repository:<br>**
git clone <url> <where to clone>
* **Retrieve the latest updates from remote repository:<br>**
git pull


To intentionally un-track sensitive files that contain non-codes related information, put their names into .gitignore file.

## Next run
