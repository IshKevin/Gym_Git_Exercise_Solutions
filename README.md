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
## Bundel 3
### Exercise 1
```bash
HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git checkout -b ft/team-page
Switched to a new branch 'ft/team-page'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git add team.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git commit -m "Add changes to team.html"
[ft/team-page 6eb37a3] Add changes to team.html
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git push origin ft/team-page
fatal: unable to access 'https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git/': Could not resolve host: github.com

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 4 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 458 bytes | 229.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/IshKevin/Gym_Git_Exercise_Solutions/pull/new/ft/team-page
remote:
To https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git checkout main
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (main)
$ git checkout -b ft/contact-page
Switched to a new branch 'ft/contact-page'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'
M       README.md

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git log
commit 6eb37a3076f5ff570ec14276d9decec6c9c27d14 (HEAD -> ft/team-page, origin/ft/team-page)
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 21 09:51:21 2023 +0200

    Add changes to team.html

commit 44c3dd789615b463a75e8950caf4b0bc1f62282b (origin/main, main, ft/contact-page)
Merge: 9a78f9c 0f33901
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:39 2023 +0200

    Merge branch 'main' of https://github.com/IshKevin/Gym_Git_Exercise_Solutions

commit 9a78f9cab27c05b4dd4ccd9eadaec18e4d4f148a
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:28 2023 +0200

    add work on readme

commit 0f3390128d5d241ff7c835f2cb9329434a269f31
:
commit 6eb37a3076f5ff570ec14276d9decec6c9c27d14 (HEAD -> ft/team-page, origin/ft/team-page)
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 21 09:51:21 2023 +0200

    Add changes to team.html

commit 44c3dd789615b463a75e8950caf4b0bc1f62282b (origin/main, main, ft/contact-page)
Merge: 9a78f9c 0f33901
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:39 2023 +0200

    Merge branch 'main' of https://github.com/IshKevin/Gym_Git_Exercise_Solutions

commit 9a78f9cab27c05b4dd4ccd9eadaec18e4d4f148a
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:28 2023 +0200

    add work on readme

commit 0f3390128d5d241ff7c835f2cb9329434a269f31

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git checkout ft/contact-page
Switched to branch 'ft/contact-page'
M       README.md

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git cherry-pick 6eb37a3076f5ff570ec14276d9decec6c9c27d14
[ft/contact-page afc2756] Add changes to team.html
 Date: Sun May 21 09:51:21 2023 +0200
 1 file changed, 14 insertions(+)
 create mode 100644 team.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git add .

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git commit -m "Add changes to contact page"
[ft/contact-page f885ec5] Add changes to contact page
 1 file changed, 5 insertions(+)

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 898 bytes | 449.00 KiB/s, done.
Total 6 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/IshKevin/Gym_Git_Exercise_Solutions/pull/new/ft/contact-page
remote:
To https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/contact-page)
$ git checkout ft/team-page
Switched to branch 'ft/team-page'

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git log
commit 6eb37a3076f5ff570ec14276d9decec6c9c27d14 (HEAD -> ft/team-page, origin/ft/team-page)
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 21 09:51:21 2023 +0200

    Add changes to team.html

commit 44c3dd789615b463a75e8950caf4b0bc1f62282b (origin/main, main)
Merge: 9a78f9c 0f33901
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:39 2023 +0200

    Merge branch 'main' of https://github.com/IshKevin/Gym_Git_Exercise_Solutions

commit 9a78f9cab27c05b4dd4ccd9eadaec18e4d4f148a
Author: IshKevin <carterk279@gmail.com>
Date:   Sun May 14 16:06:28 2023 +0200

    add work on readme

commit 0f3390128d5d241ff7c835f2cb9329434a269f31
Merge: a73115b c3f61c6

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git revert  6eb37a3076f5ff570ec14276d9decec6c9c27d14
[ft/team-page 67ffcfb] Revert "Add changes to team.html"
 1 file changed, 14 deletions(-)
 delete mode 100644 team.html

HP@KEVIN MINGW64 ~/Documents/web tech/Gym_Git_Exercise_Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 4 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 260 bytes | 260.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/IshKevin/Gym_Git_Exercise_Solutions.git
   6eb37a3..67ffcfb  ft/team-page -> ft/team-page
```