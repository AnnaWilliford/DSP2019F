**Anna Williford**

### Problem Part2.A
```bash
$ git branch test1
$ git branch test2
```

### Problem Part2.B
```bash
$ git checkout test1
Switched to branch 'test1'

#create new file
$ touch test.txt
```

### Problem Part2.C
```bash
$ echo "This is some example text for branch test1" > test.txt
```

### Problem Part2.D
```bash
$ git add --all
$ git commit -m "add test.txt to branch test1"

[test1 5c28361] add test.txt to branch test1
 3 files changed, 24 insertions(+), 1 deletion(-)
 delete mode 100644 Homework/HW1.txt
 create mode 100644 Homework/VCS/test.txt
```

### Problem Part2.E
```bash
$ git checkout test2
Switched to branch 'test2'
$ ls
```
There is no test.txt file on branch test2 because when this branch was created, it copied master branch that did not contain test.txt

### Problem Part2.E
```bash
$ touch test.txt
$ echo "This is some example test for branch test2 to its content" > test.txt
```
### Problem Part2.G
```bash
$ git checkout test1
error: The following untracked working tree files would be overwritten by checkout:
	Homework/VCS/test.txt
Please move or remove them before you switch branches.
Aborting
```
To fix, add and commit test.txt to branch test2
```bash
$ git add --all
$ git commit -m "add test.txt to branch test2"
[test2 1065b31] add test.txt to branch test2
 1 file changed, 1 insertion(+)
 create mode 100644 Homework/VCS/test.txt
$ git checkout test1
Switched to branch 'test1'
```

### Problem Part2.G
```bash
$ git checkout master
Switched to branch 'master'
$ git merge test1
Removing Homework/HW1.txt
Merge made by the 'recursive' strategy.
 Homework/HW1.txt      | 1 -
 Homework/VCS/test.txt | 1 +
 2 files changed, 1 insertion(+), 1 deletion(-)
 delete mode 100644 Homework/HW1.txt
 create mode 100644 Homework/VCS/test.txt 
```

### Problem Part2.I

Now test.txt is on master in Homework/VCS

### Problem Part2.J

```bash
$ git merge test2
Auto-merging Homework/VCS/test.txt
CONFLICT (add/add): Merge conflict in Homework/VCS/test.txt
Automatic merge failed; fix conflicts and then commit the result.
```
We get an error because test.txt in master branch from test1 branch and test.txt in branch test2 have different content. Git does not know which test.txt should be merged.

### Problem Part2.K
```bash
$ git checkout test2
Homework/VCS/test.txt: needs merge
error: you need to resolve your current index first
```

### Problem Part2.L
```bash 
$ git status
On branch master
Your branch is ahead of 'origin/master' by 7 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both added:      test.txt

no changes added to commit (use "git add" and/or "git commit -a")
```

There are unmerged paths...

### Problem Part2.M
Open test.txt in master branch, fixed conflict within the file to:
"This is some example text from both test1 and test2 branches combined."
Saved.

### Problem Part2.N
```bash
$ git status
On branch master
Your branch is ahead of 'origin/master' by 7 commits.
  (use "git push" to publish your local commits)

You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)

	both added:      test.txt

no changes added to commit (use "git add" and/or "git commit -a")

$ git add --all
$ git commit -m "fixed conflict in test.txt"

$ git checkout test2
Switched to branch 'test2'
```

### Problem Part2.O
```bash
$ git branch -d test1
error: The branch 'test1' is not fully merged.
If you are sure you want to delete it, run 'git branch -D test1'.
```
I did not merge test1 to test2, cannot delete branch from test2

### Problem Part2.P
```bash
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 9 commits.
  (use "git push" to publish your local commits)

$ git branch -d test1
Deleted branch test1 (was da925ea).

$ git branch
  development
* master
  test2
```

### Problem Part2.Q

Q: Why is there such a difference in Git messages between when you tried deleting test1 branch from test2 branch, and when you tried deleting test1 branch from master branch?

A: I did not merge test1 with test2, but i did merge test1 with master

### Problem Part2.R
```bash
$ git checkout test2
Switched to branch 'test2'
$ git branch -d test2
error: Cannot delete branch 'test2' checked out at '/Users/annawilliford/Desktop/Anya/Git/DSP2019F'
```

### Problem Part2.S
```bash
$ git checkout master
Switched to branch 'master'
Your branch is ahead of 'origin/master' by 9 commits.
  (use "git push" to publish your local commits)
$ 
Deleted branch test2 (was 1065b31).
$ git branch
  development
* master
```
### Problem Part2.T
```bash
$ git status
On branch master
Your branch is ahead of 'origin/master' by 9 commits.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
```
**Note** the content of this file was created as I worked through the problems. Now I copy this content to readme.md on master branch and commit changes. Then push to remote.

```bash
$ git add --all
$ git commit -m "recorded answers to questions in readme.md in Homework/VCS"
$ git push
```
