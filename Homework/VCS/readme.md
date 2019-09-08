Anna Williford


### Problem Part2.A
```bash
$ git branch test1
$ git branch test2
```

### Problem Part2.B
```bash
$ git checkout test1
Switched to branch 'test1'

#creat new file
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