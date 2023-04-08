# Interactive reabase

## Git rebase command:
```bash
git rebase -i origin/develop   
```
here origin/develop is the branch agains which we are going to rebase, -i is flag for interactive

## stashing

Now it would all the commits behind the origin/develop branch we have to mark the commits which need 
to be stashed and remain the single commit as rebase where all the other commits would be stashed

```bash
pick 1a2sd3s commit-1
pick 2sl3ll4 commit-2
pick 73sdsfk commit-3
pick 8k97sdf commit-4
```

* Press insert button to start typing.
* mark as s for the commits we wants to stash

```bash
pick 1a2sd3s commit-1
s 2sl3ll4 commit-2
s 73sdsfk commit-3
s 8k97sdf commit-4
```
* press esc key
* type :wq to save and complete rebase (:q to avoid changes and complete rebase)

## Resolve conflicts.

* If we have any conflicts we have to resolve it and commit the changes and we have to continue rebase

 ```bash
 git rebase --continue
 ```
 We need to perform this step untill we resolve all the commits. once all the conflicts resolved, we will
 get the message as rebase completed.
 
## Force push

Since we are manually changed the tree, we could not normal push but we have to do foce push.

```bash
git push -f
```

