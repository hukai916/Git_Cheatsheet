# Git usage cheat sheet
## Basics
* **Install Git:<br>**
conda install git
* **Check Git version:<br>**
git --version
* **Check Git configuration:<br>**
git config --list
* **Check Git command help:<br>**
git config --help
* Initiate a new git under the same folder<br>
git init
* Config the username and email for first usage:<br>
git config --global user.name 'Kai Hu'
git config --global user.email 'hukai916@gmail.com'
* Add to the staging/index for future commit:<br>
git add
* Submit to local repository:<br>
git commit
* Submit to remote repository: (use SH key to ignore user info input)<br>
git push
* Retrieve the latest from remote repository:<br>
git pull
* Clone the remote repository into a new directory:<br>
git clone
* Add file to staging status:<br>
git add
* Remove file from staging status:<br>
git rm --cached <file>
* Add all files to staging status:<br>
git add .

Note that when you change staged files, and do git status to check their status, they will be listed as changed too.

## Branching
To create a branch, first commit all changes, then (if you are working on your own projects, you don't even need to use branches)<br>
* Create new branch:<br>
git branch branch_name
* Switch branches:<br>
git checkout branch_name
* Merge branches:<br>
git merge branch_name

## Remote repository
* Get a list of remote repositories:<br>
git remote
* Submit local branch to remote repository:<br>
git remote add origin https://github.com/hukai916/Git_cheat_sheet.git

Note that "origin" the assigned name for remote repository.

* Submit master branch to remote repository:<br>
git push -u origin master https://github.com/hukai916/Git_cheat_sheet.git
