# COMMANDS

## Basic Commands

- git init        
  > to start a proyect
- git add .
  > to add files to the staging 
- git commit -m "message to the commmit"
  > to send the commit
- git status
- git status -s
- git status -s -b
- git log 
- git show
- git show <filename.extention>
- git --version
- git rm <filename.extention>
  > to remove from the staging
- git diff <id_commit1> <id_commit2>
- git commit -am "mensaje"
- git commit -amend -> to modify the last commit message 
- git checkout -- . -> remove from staging
- git checkout --  README.md -> remove from staging
- git push origin master
- git pull origin master --allow-unrelated-histories
  > when you create a rep in github and you want to join all histories with a local repo to then push later to that repo

## Logging
	
	- git log --oneline --decorate --all --graph
	- git log --oneline 
	
## Moving to specific time
	
	- git reset --soft 89rfgr87 -> keep changes in staging
	- git reset --mixed 851c2  -> keep changes out of staging, in local
	- git reset --hard 89rfgr87 -> go to specific commit without changes
	- git reflog  -> to see all commits done
	- git config core.autocrlf true


## Global Config

- git config
- git config --global -e 
- git config -l
  > to see global settings
- git config --list --show-origin
  > to show detail about location settings
- git config --global user.name "gossio"
- git config --global user.email "email"

### Connection to GIT
- git remote -v
  > to see origin
 
 #### HTTPS
 
- git remote add origin {https-url}
  > to set remote origin to manage the project by https connection

#### SSH

- git remote set-url origin {ssh-url}
  > setting a remote rep by SSH instead of HTTPS

## Setting up SSH keys in local

- ssh-keygen -t rsa -b 4096 -C "your-email"
  > execute it in user home path: cd ~ or home/user, i.e gossio/.ssh

### Windows

- eval $(ssh-agent -s)
  > to start a ssh agent
- ssh-add ~/.ssh/id_rsa
  > to add private key to a local machine

### MAC

- eval "$(ssh-agent -s)"
- vim config
  > It is needed to create a file in ~/.ssh || i.e cd .ssh
  > add this content: 
  > Host *
  >       AddKeysToAgent yes
  >       UseKeychain yes
  >       IdentityFile ~/.shh/id_rsa 
  >       "To exit: esc + shift + z-z"
- ssh-add -K ~/.shh/id_rsa
