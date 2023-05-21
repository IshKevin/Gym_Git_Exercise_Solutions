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
HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git commit -m"back to orig"
[main 9102266] back to orig
 4 files changed, 117 insertions(+)
 create mode 100644 about.js
 create mode 100644 home.htm
 create mode 100644 team.js

```
### Exercise 3
```bash
HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/bundle-2)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git pull
remote: Enumerating objects: 1, done.
remote: Counting objects: 100% (1/1), done.
remote: Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (1/1), 621 bytes | 0 bytes/s, done.
From https://github.com/IshKevin/Gym_Git_Exercise_Solutions
   9c9f80b..a73115b  main       -> origin/main
Updating 9c9f80b..a73115b
Fast-forward
 service.html | 12 ++++++++++++
 1 file changed, 12 insertions(+)
 create mode 100644 service.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git checkout -b ft/service-redesign
Switched to a new branch 'ft/service-redesign'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/service-redesign)
$ git add service.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/service-redesign)
$ git commit -m"fix service in sev-red"
[ft/service-redesign c3f61c6] fix service in sev-red
 1 file changed, 1 insertion(+), 1 deletion(-)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/service-redesign)
$ git push --set-upstream origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 320 bytes | 160.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/IshKevin/Gym_Git_Exercise_Solutions/pull/new/ft/service-redesign
remote:
To https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign
branch 'ft/service-redesign' set up to track 'origin/ft/service-redesign'.

```

## Bundle 3
### Exercise 1
```bash

