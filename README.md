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
- to get changed data from G 	itHub to local machine: `git pull`
#### Open Git GUI (User Interface)
- run in Git Bash command `git gui&`
#### Open Git history commits in GUI
- run in Git Bash command `git gitk&`
## Undoing changes
![Git undoing changes](./assets/image-1.png)

**Working directory (before you apply `git add .`)**
- `git checkout -- README.md` - this command undoing all changes in file `README.md`
-  `git checkout .` - this command undoing all changes in all files
-  `git clean -xdf ` - this command delete all files that were not previously committed

**Staging area (after `git add .`)**
- `git reset -- README.md` - this command return file to stage before `git add .`

**Local branch (afrer `git commit -m "commit here"`)**
- `git reset HEAD~1` - this command remove last commit **HEAD~(1)** -it is last commit if you want remove **2** last commit you should use `git reset HEAD~2`
- `git commit --amend -m "commit message"` - allow us add additional commit to previous commit, you may also do this via `git gui&`

**Remot repository**
- `git revert <sha1>`

## Git reset
![Git reset](./assets/image.png)

- `git reset --soft HEAD~1` - reset last one commit and return to after `git add .` stage
- `git reset --mixed HEAD~1` - reset last one commit and return to before `git add .` stage
- `git reset --hard HEAD~1` - remove totally last one commit
