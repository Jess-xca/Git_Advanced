# Git_Advanced

## Ex 1

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git clone git@github.com:Jess-xca/Git_Advanced.git
Cloning into 'Git_Advanced'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Receiving objects: 100% (3/3), done.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ touch test{1..4}.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git add test1.md && git commit -m "chore: Create initial file"
[main 5c23313] chore: Create initial file
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 test1.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git add test2.md && git commit -m "chore: Create another file"
[main 19d65d5] chore: Create another file
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 test2.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git add test3.md && git commit -m "chore: Create third and fourth files"
[main bb4a26a] chore: Create third and fourth files
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 test3.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git status
On branch main
Your branch is ahead of 'origin/main' by 3 commits.
(use "git push" to publish your local commits)

Untracked files:
(use "git add <file>..." to include in what will be committed)
test4.md

nothing added to commit but untracked files present (use "git add" to track)
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced/Git_Advanced (main)
$ git log
commit bb4a26af673147631de724f76bad429cebc8194b (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date: Wed Feb 26 12:56:03 2025 +0200

    chore: Create third and fourth files

:

- History restored
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE (main)
$ cd Git_Advanced
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add test4.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git commit --amend -m "chore: Add test4.md to the commit"
[main cc8d0a1] chore: Add test4.md to the commit
Date: Wed Feb 26 12:56:03 2025 +0200
2 files changed, 0 insertions(+), 0 deletions(-)
create mode 100644 test3.md
create mode 100644 test4.md
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git push
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (7/7), 683 bytes | 24.00 KiB/s, done.
Total 7 (delta 2), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (2/2), done.
To github.com:Jess-xca/Git_Advanced.git
537e8bb..cc8d0a1 main -> main
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git push --force
Everything up-to-date
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```

### Ex 2

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git restore <file>..." to discard changes in working directory)
modified: README.md

reword cc8d0a1 chore: Add test4.md to the commit
the commit.

#

# Date: Wed Feb 26 12:56:03 2025 +0200

#

# Date: Wed Feb 26 12:56:03 2025 +0200

#

chore: Add test4.md to the commit

# Please enter the commit message for your changes. Lines starting

chore: Add test4.md to the commit
chore: Add test4.md to the commit
chore: Add test4.md to the commit
chore: Add test4.md to the commit
(main)
$ git commit -m "Save changes before rebasing"
[main ed4ef1a] Save changes before rebasing
1 file changed, 128 insertions(+), 1 deletion(-)

user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main)
$ git rebase -i HEAD~2
hint: Waiting for your editor to close the file... Vim:
Error reading input, exiting...
Vim: preserving files...
Vim: Finished.

error: there was a problem with the editor 'vi'
Please supply the message using either -m or -F option.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main|REBASE 1/2)
$ git rebase -i HEAD~2
fatal: It seems that there is already a rebase-merge directory, and
I wonder if you are in the middle of another rebase. If that is the
case, please try
git rebase (--continue | --abort | --skip)
If that is not the case, please
rm -fr ".git/rebase-merge"
and run me again. I am stopping in case you still have
something
valuable there.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main|REBASE 1/2)
$ git rebase --continue
Successfully rebased and updated refs/heads/main.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git rebase -i HEAD~4
[detached HEAD f7c55f2] chore: Create second file
Date: Wed Feb 26 12:55:56 2025 +0200
1 file changed, 0 insertions(+), 0 deletions(-)
create mode 100644 test2.md
Successfully rebased and updated refs/heads/main.
```

### Ex 3

```bash
user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git rebase -i HEAD~3
[detached HEAD 8fea62a] Save changes before rebasing
 Date: Fri Feb 28 11:11:35 2025 +0200
 1 file changed, 387 insertions(+), 1 deletion(-)
Successfully rebased and updated refs/heads/main.

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git status
On branch main
Your branch and 'origin/main' have diverged,
and have 2 and 3 different commits each, respectively.
  (use "git pull" if you want to integrate the remote branch with yours)

nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add .

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git rebase --continue
fatal: no rebase in progress

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git push origin main --force
Enumerating objects: 8, done.
Counting objects: 100% (8/8), done.
Delta compression using up to 4 threads
Compressing objects: 100% (6/6), done.
Writing objects: 100% (6/6), 2.30 KiB | 1.15 MiB/s, done.
Total 6 (delta 3), reused 0 (delta 0), pack-reused 0 (from 0)
remote: Resolving deltas: 100% (3/3), completed with 1 local object.
To github.com:Jess-xca/Git_Advanced.git
 + 3b12e48...1653cda main -> main (forced update)
```

#### Ex 4

```bash
user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git reset --soft c7f2ef5^

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add test3.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git commit -m "Added test3.md"
[main d06fe77] Added test3.md
 3 files changed, 433 insertions(+), 1 deletion(-)
 create mode 100644 test3.md
 create mode 100644 test4.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add test4.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git commit -m "Added test4.md"
On branch main
Your branch and 'origin/main' have diverged,
and have 1 and 4 different commits each, respectively.

nothing to commit, working tree clean

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git reset --soft c7f2ef5^

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git status
On branch main
Your branch is behind 'origin/main' by 4 commits, and can be fast-forwarded.
  (use "git pull" to update your local branch)

Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   README.md
        new file:   test3.md
        new file:   test4.md


user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add test3.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git reset test4.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git commit -m "Added test3.md"
[main 1932ffb] Added test3.md
 2 files changed, 433 insertions(+), 1 deletion(-)
 create mode 100644 test3.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git add test4.md

user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git commit -m "Added test4.md"
[main 10f4aba] Added test4.md
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test4.md
```
