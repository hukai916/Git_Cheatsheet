# Git usage cheat sheet
## install Git:
conda install git
## check Git version:
git --version
## check Git configuration:
git config --list
## check Git command help:
git config --help
## initiate a new git under the same folder
git init
## config the username and email for first usage:
git config --global user.name 'Kai Hu'
git config --global user.email 'hukai916@gmail.com'
## add to the staging/index for future commit:
git add
## submit to local repository:
git commit
## submit to remote repository: (use SH key to ignore user info input)
git push
## retrieve the latest from remote repository:
git pull
## clone the remote repository into a new directory:
git clone
## Add file to staging status:
git add
## Remove file from staging status:
git rm --cached <file>
## Add all files to staging status:
git add .

Note that when you change staged files, and do git status to check their status, they will be listed as changed too.
## to create a branch, first commit all changes, then (if you are working on your own projects, you don't even need to use branches)
git branch branch_name
git checkout branch_name # this would switch to branch_name
git merge branch_name

## working with remote repository
git remote # get a list of remote repositories
git remote add origin https://github.com/hukai916/Git_cheat_sheet.git # add remote repository named origin
git push -u origin master https://github.com/hukai916/Git_cheat_sheet.git # submit the master branch to remote repository
