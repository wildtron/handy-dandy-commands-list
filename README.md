wildtron's Handy Dandy Commands List 
---

git
---

1. delete tag in remote
```
    git push --delete origin <tag-name>
```

2. delete tag locally
```
    git tag -d <tag-name>
```

man
---
1. view command's manual
```
    man <command>
```

mysqldump
---

1. create dumps without locking tables
```
    mysqldump --single-transaction --quick ...<other-flags>
```

xclip
---

1. print content of clipboard to stdout
```
    xclip -sel c -o stdout
```
