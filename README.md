# Gym-Git-Exercise-Solutions

## Bundle 1

### Exercise 1

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions
$ git init
Initialized empty Git repository in C:/Users/gsngd/Documents/Gym-Git-Exercise-Solutions/.git/

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ echo "The branch is already called main by default"
The branch is already called main by default

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ echo "This is a test" > test.txt

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git add .
warning: in the working copy of 'test.txt', LF will be replaced by CRLF the next time Git touches it
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git commit -m "initial commit"
[main (root-commit) 0df72c0] initial commit
 1 file changed, 1 insertion(+)
 create mode 100644 test.txt

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git remote add origin https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git push origin main
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Writing objects: 100% (3/3), 218 bytes | 218.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      main -> main

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git branch dev

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git switch dev
Switched to branch 'dev'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git branch test

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git switch dev
Already on 'dev'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git branch -d test
Deleted branch test (was 0df72c0).
```

### Exercise 2

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch home.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch about.hmtl

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ rm about.hmtl

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)
$ touch about.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
No local changes to save

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add about.html 

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ touch team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git add team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash
Saved working directory and index state WIP on dev: 0df72c0 initial commit

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html

Dropped stash@{1} (c9a55d0aec5aafa0f2162356d4098431ae08863e)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop stash@{1}
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   about.html
        new file:   home.html

Dropped stash@{1} (8710265a403dc58299b7ca61c95c92080c628a6e)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git commit -m "Add about and home html file"
[dev cb5d1f5] Add about and home html file
 2 files changed, 22 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git push origin dev
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (4/4), done.
Writing objects: 100% (4/4), 528 bytes | 528.00 KiB/s, done.
Total 4 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), done.
remote: 
remote: Create a pull request for 'dev' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/dev
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      dev -> dev

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git stash pop
On branch dev
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   team.html

Dropped refs/stash@{0} (2b29310c3a55c36b0ad72446fabb758572e8ac56)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)       
$ git reset --hard
HEAD is now at cb5d1f5 Add about and home html file
```


## Bundle 2

### Exercises 1

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)
$ git branch ft/bundle-2

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (dev)
$ git switch ft/bundle-2 
Switched to branch 'ft/bundle-2'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ touch services.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git commit -m "feat: add service html file"
[ft/bundle-2 e744d77] feat: add service html file
 1 file changed, 11 insertions(+)
 create mode 100644 services.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/bundle-2)
$ git push origin ft/bundle-2
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 512 bytes | 512.00 KiB/s, done.
Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
remote: 
remote: Create a pull request for 'ft/bundle-2' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/ft/bundle-2
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/bundle-2 -> ft/bundle-2

```

### Exercise 2

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git branch
  dev
  ft/bundle-2
* main

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git pull
remote: Enumerating objects: 4, done.
remote: Counting objects: 100% (4/4), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (2/2), 712 bytes | 101.00 KiB/s, done.
From https://github.com/gsngdavid/Gym-Git-Exercise-Solutions
   35e2e78..1b7f8d9  main       -> origin/main
Updating 35e2e78..1b7f8d9
Fast-forward
 about.html    | 11 +++++++++++
 home.html     | 11 +++++++++++
 services.html | 11 +++++++++++
 3 files changed, 33 insertions(+)
 create mode 100644 about.html
 create mode 100644 home.html
 create mode 100644 services.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git branch ft/service-redesign

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git commit -m "feat: add a paragraph to the services.html"
[ft/service-redesign 75f579b] feat: add a paragraph to the services.html
 1 file changed, 1 insertion(+)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 361 bytes | 361.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
remote:
remote: Create a pull request for 'ft/service-redesign' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/ft/service-redesign   
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/service-redesign -> ft/service-redesign

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git commit -m "feat: add paragraph to services.html"
[main eff051b] feat: add paragraph to services.html
 1 file changed, 1 insertion(+)

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 360 bytes | 360.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
   1b7f8d9..eff051b  main -> main

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)      
$ git switch ft/service-redesign
Switched to branch 'ft/service-redesign'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git diff main
diff --git a/services.html b/services.html
index bcb81ac..86c1ac0 100644
--- a/services.html
+++ b/services.html
@@ -7,6 +7,6 @@
 </head>
 <body>
     <h1>This is services page</h1>
-    <p>Changes to services.htm form main branch</p>
+    <p>This is some changes to services page.</p>
 </body>
 </html>
\ No newline at end of file

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git merge main
Auto-merging services.html
CONFLICT (content): Merge conflict in services.html
Automatic merge failed; fix conflicts and then commit the result.

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign|MERGING)
$ git commit -m "feat: Resolve conflicts"
[ft/service-redesign a3b8242] feat: Resolve conflicts

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/service-redesign)
$ git push origin ft/service-redesign 
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 387 bytes | 387.00 KiB/s, done.
Total 3 (delta 2), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (2/2), completed with 2 local objects.
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
   75f579b..a3b8242  ft/service-redesign -> ft/service-redesign


```


## Bundle 3

### Exercise 1

```bash
gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git branch ft/team-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git switch ft/team-page
Switched to branch 'ft/team-page'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ touch team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git add team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git commit -m "feat: Add team page"
[ft/team-page d43cd9e] feat: Add team page
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git push origin ft/team-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 432 bytes | 432.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/team-page' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/ft/team-page
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/team-page -> ft/team-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git switch main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git branch ft/contact-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (main)
$ git switch ft/team-page
Switched to branch 'ft/team-page'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git log
commit d43cd9e3c493c4c4484f5a78e4dd82ed5397e9a3 (HEAD -> ft/team-page, origin/ft/team-page)
Author: gsngdavid <gsngdavid@gmail.com>
Date:   Thu Jul 27 11:00:50 2023 +0200

    feat: Add team page

commit 773b6de93831cd90f8bed8ac8b2f72fd7b978d8f (origin/main, main, ft/contact-page)
Author: gsngdavid <gsngdavid@gmail.com>
Date:   Wed Jul 26 13:02:30 2023 +0200

    feat: Complete Bundler 2 | Exercise 2

commit eff051ba81513e5222e689fe214b9ba4846c6568
Author: gsngdavid <gsngdavid@gmail.com>
Date:   Wed Jul 26 12:46:26 2023 +0200

    feat: add paragraph to services.html

commit 1b7f8d96053f268d556f39019b33e2b3dada3484

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/team-page)
$ git switch ft/contact-page
Switched to branch 'ft/contact-page'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git cherry-pick d43cd9e3c493c4c4484f5a78e4dd82ed5397e9a3
[ft/contact-page b52e531] feat: Add team page
 Date: Thu Jul 27 11:00:50 2023 +0200
 1 file changed, 11 insertions(+)
 create mode 100644 team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ touch contact.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git commit -m "feat: Add contact page"
[ft/contact-page 241f326] feat: Add contact page
 1 file changed, 11 insertions(+)
 create mode 100644 contact.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git push origin ft/contact-page
Enumerating objects: 7, done.
Counting objects: 100% (7/7), done.
Delta compression using up to 12 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 694 bytes | 694.00 KiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/contact-page' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/ft/contact-page       
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/contact-page -> ft/contact-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git branch ft/faq-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/contact-page)
$ git switch ft/faq-page
Switched to branch 'ft/faq-page'

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ touch faq.hmtl

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ mv faq.hmtl faq.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git add .

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git commit -m "feat: Add faq page"
[ft/faq-page d473f67] feat: Add faq page
 1 file changed, 11 insertions(+)
 create mode 100644 faq.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 12 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 431 bytes | 431.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote:
remote: Create a pull request for 'ft/faq-page' on GitHub by visiting:
remote:      https://github.com/gsngdavid/Gym-Git-Exercise-Solutions/pull/new/ft/faq-page
remote:
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
 * [new branch]      ft/faq-page -> ft/faq-page

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git revert d43cd9e3c493c4c4484f5a78e4dd82ed5397e9a3
[ft/faq-page cb3164b] Revert "feat: Add team page"
 1 file changed, 11 deletions(-)
 delete mode 100644 team.html

gsngd@David MINGW64 ~/Documents/Gym-Git-Exercise-Solutions (ft/faq-page)
$ git push origin ft/faq-page
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 12 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 275 bytes | 275.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/gsngdavid/Gym-Git-Exercise-Solutions.git
   d473f67..cb3164b  ft/faq-page -> ft/faq-page

```