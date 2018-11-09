# Notes for basic Git usage
## install Git:
conda install git
## check Git version:
git --version
## check Git configuration:
git config --list
## check Git command help:
git config --help
## setup git default text editor to nano:
git config --global core.editor 'nano's
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
## Add all file to staging status:
git add .

Note that when you change staged files, and do git status to check their status, they will be listed as changed too.

## to edit git commit comment:
git commit
