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