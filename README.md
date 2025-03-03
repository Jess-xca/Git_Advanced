# Git_Advanced

## Part 1

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

### Part 2

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
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main)
$ git rebase -i HEAD~2
Successfully rebased and updated refs/heads/main.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced
(main)
$ git rebase -i HEAD~4
hint: Waiting for your editor to close the file... Vim:
Error reading input, exiting...
Vim: Finished.

error: there was a problem with the editor 'vi'
Please supply the message using either -m or -F option.
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main|REBASE 2/4)
$ git rebase --abort
```

```bash
user@\_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git rebase --abort
fatal: no rebase in progress
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

```bash
user@_26026 MINGW64 ~/Desktop/GIT-EXERCISE/Git_Advanced (main)
$ git log
commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing

commit c7f2ef5bea84171ce3716471467e41f0cce91026
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Wed Feb 26 12:56:03 2025 +0200
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing

commit c7f2ef5bea84171ce3716471467e41f0cce91026
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Wed Feb 26 12:56:03 2025 +0200







commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD






commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing

commit c7f2ef5bea84171ce3716471467e41f0cce91026
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing

commit c7f2ef5bea84171ce3716471467e41f0cce91026





commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main




commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing




commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing

commit c7f2ef5bea84171ce3716471467e41f0cce91026
Author: Jessica Irakoze <jessicairakoze4@gmail.com>

Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

    Save changes before rebasing




commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>




Date:   Fri Feb 28 11:11:35 2025 +0200

Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200




commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200




commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200


commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200


commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200


Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200


commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main

commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main
commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200
commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
commit 319acf0492007338dedd06bfc20adcf893dc5aff (HEAD -> main)
Author: Jessica Irakoze <jessicairakoze4@gmail.com>
Date:   Fri Feb 28 11:11:35 2025 +0200

```

### Part 3
