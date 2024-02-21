# git-demo - Repository to learn github commands

#### Git Setup
1) You can download [git here](http://git-scm.com/downloads)
2) Install Git with default settings.

***Generating a pair of ssh keys:***
1) open Git Bash and run script `ssh-keygen -t rsa –C “mail@test.com"` where 'mail@test.com' it is your github email
2) ssh-keys will generated and savad in folder `C:/Users/User_Name/.ssh` where `id_rsa.pub` it is public key that you should use in github  profile settings
The public key (id_rsa) should be sent to the owner of the repository in order to obtain work rights. Or upload to profile settings in bitbucket / github / gitlab.

***Username and email settings:***
1) add git config username: `git config --global user.name “FirstName SecondName“`
2) add git config email: `git config --global user.email “mail@test.com"`

#### Clone GitHub repository to local machine
1) open Git Bash in folder where you want to copy repository
2) run command:  `git clone git@github.com:gudzsv/git-demo.git` where `git@github.com:gudzsv/git-demo.git` - it is **SSH** link to repository you want to clone
#### How to Add changes from local machine to GitHub
1) check if you have changed files on local machine:  `git status`
2) add all changed files: `git add .` or if you have to add one file: `git add filename.txt`
3) add files to commit, you should use this command: `git commit -m "coment here"`
4) check commit logs: `git log`
5) send changed data from local machine to GitHub: `git push`
#### Get changed files fom GitHub to local machine
1) to get changed data from GitHub to local machine: `git pull`
