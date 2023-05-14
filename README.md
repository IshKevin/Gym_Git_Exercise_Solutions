# Gym_Git_Exercise_Solutions
## Bundle 1
### Exercise 1
```bash
HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions
$ git init
Initialized empty Git repository in C:/Users/HP/Documents/web tech/Gym_Git_Exercise_Solutions/.git/

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (master)
$ git branch -m master main

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add README.md

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git commit -m"add README.md file"
[main (root-commit) b6cf148] add README.md file
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 README.md

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git remote add origin https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git push -u origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 222 bytes | 111.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git checkout -b dev
Switched to a new branch 'dev'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (dev)
$ git checkout -b test
Switched to a new branch 'test'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (test)
$ git checkout dev
Switched to branch 'dev'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (dev)
$ git branch -d test
Deleted branch test (was b6cf148).

```

### Exercise 2
```bash
HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash list

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        home.htm

nothing added to commit but untracked files present (use "git add" to track)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 4724d39 remove all

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 4724d39 remove all

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash
Saved working directory and index state WIP on main: 4724d39 remove all

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash list
stash@{0}: WIP on main: 4724d39 remove all
stash@{1}: WIP on main: 4724d39 remove all
stash@{2}: WIP on main: 4724d39 remove all

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.js

Dropped stash@{1} (4859c50347129ec71cb189dc9081813610e5342e)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash pop stash@{1}
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.js
        new file:   home.htm

Dropped stash@{1} (5d495e3b1aa2c27b42cd8c05becc97a4a0cc7e5e)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git commit -m"restore files"
[main 64ed566] restore files
 2 files changed, 13 insertions(+)
 create mode 100644 about.js
 create mode 100644 home.htm

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash list
stash@{0}: WIP on main: 4724d39 remove all

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git stash pop stash@{0}
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 1 different commits each, respectively.
  (use "git pull" to merge the remote branch into yours)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.js

Dropped stash@{0} (4f2dba8fc17e59902270b067bd1245b6abeb997b)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git reset HEAD~
```