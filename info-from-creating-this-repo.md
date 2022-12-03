
max@m20:~$ cd y
max@m20:~/y$ ls -d ci*
cicd01-hello
max@m20:~/y$ mkdir cicd02-workspace
max@m20:~/y$ cd cicd02-workspace/
max@m20:~/y/cicd02-workspace$ mkdir .circleci
max@m20:~/y/cicd02-workspace$ cd .circleci/
max@m20:~/y/cicd02-workspace/.circleci$ touch config.yml
max@m20:~/y/cicd02-workspace/.circleci$ cd ..
max@m20:~/y/cicd02-workspace$ touch README.md
max@m20:~/y/cicd02-workspace$ code .
max@m20:~/y/cicd02-workspace$ git init -b main
error: unknown switch `b'
...
note:
If you’re using Git 2.28.0 or a later version, you can set the name of the default branch using -b.

max@m20:~/y/cicd02-workspace$ git version
git version 2.25.1
max@m20:~/y/cicd02-workspace$ git init
Initialized empty Git repository in /home/max/y/cicd02-workspace/.git/
max@m20:~/y/cicd02-workspace$ git status
Untracked files:
	.circleci/
	README.md
max@m20:~/y/cicd02-workspace$ git add .
max@m20:~/y/cicd02-workspace$ git status
Changes to be committed:
	new file:   .circleci/config.yml
	new file:   README.md

max@m20:~/y/cicd02-workspace$ git commit -m "initial/first commit"
[master (root-commit) 717fd52] initial/first commit
 2 files changed, 52 insertions(+)
 create mode 100644 .circleci/config.yml
 create mode 100644 README.md
max@m20:~/y/cicd02-workspace$ git branch -a
* master
max@m20:~/y/cicd02-workspace$ git branch -M main

try not to use master anymore !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!
max@m20:~/y/cicd02-workspace$ git branch -a
* main

max@m20:~/y/cicd02-workspace$ git remote add origin git@github.com:mc1496/cicd02-workspace.git
max@m20:~/y/cicd02-workspace$ git push -u origin main
ERROR: Repository not found.
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.

create empty repo in github as cicd02-workspace

max@m20:~/y/cicd02-workspace$ git remote add origin git@github.com:mc1496/cicd02-workspace.git
fatal: remote origin already exists.


max@m20:~/y/cicd02-workspace$ git push -u origin main
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 6 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (5/5), 895 bytes | 895.00 KiB/s, done.
Total 5 (delta 0), reused 0 (delta 0)
To github.com:mc1496/cicd02-workspace.git
 * [new branch]      main -> main
Branch 'main' set up to track remote branch 'main' from 'origin'.
max@m20:~/y/cicd02-workspace$ 


