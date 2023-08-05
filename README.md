# Github control using terminal/cli

This file will guide how to start with github and control it through terminal 

## Installation

Create your account in github\
Create repository(any name for ex- demo-repo) 

### Terminal commands
*  check the files of hidden folder(ssh) in home directory 
```
>> ls -la ~/.ssh
```
* Register the keygen to generate private/public pair of files in above folder.

    files are - ***id_rsa, id_rsa.pub***
```
>> ssh-keygen -t rsa -b 4096 -C "your email"
```
* Read data from file id_rsa.pub created above. Copy content (SSH key) of this file into SSH key section of github that will be found under ***profile->setting-> SSH and GPG keys -> SSH Keys*** to link key with your account  
```
>> cat ~/.ssh/id_rsa.pub
```
* make folder (any name for ex- git) and clone repository(you created demo-repo) in above installation part
```
>> mkdir git
>> git clone git@github.com:githubyourprofilename/reponame.git
```
### start with code version
* create blank file using nano command and .md is markdown for lightweight formatting
```
>> nano READM.md
```
* lets save this file in github  and [dot] means all file, you can specify filename also
```
# you will know which branch you are pointing to
>> git branch

# you will know what changes not staged for commit
>> git status

# you can create branch from main branch and commit there instead of direct to main
>> git checkout -b branchname

# which files you are going to stage for commit
>> git add .
# if above files are need to unstage (ignore for now)
>> git restore .

# stage files to commit
>> git commit -m 'any messages'

# git push change to github server
>> git push -u origin/HEAD

# to sync your local repo with github server main branch
>> git pull
```
