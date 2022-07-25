# GitCommands
Commonly used Git commands

```bash
git status # to know the current status of the repo
git add . # adding all the files to stage
git commit -m "my comments" # to commit the staged changes with a message
git push # to push the changes to server
```

4 Most Common Git Mistakes

* <b>Discard changes to local files in git</b>
As a programmer, it happens every day that unexpected errors occur. To solve the errors quickly, 
we fumble wildly with the code. Unfortunately, these code changes are not always optimal. It is, 
therefore, helpful to quickly undo the changes you have made. this is the common mistake in git.
if you don't want to do it you can do git commit with a comment.
With the command “git checkout” you can reset the files to their original state:

```bash
"myCode" git checkout - myCode # Reset directory 
```

* Undo local commits. git commit revert
You have already created four new commits and only now realize that one of these commits contains a 
major error. Oops!

No panic. If you want to undo one or more commits, you can use the “git reset” command. The command knows three different modes (soft, hard, mixed):

```bash
git reset HEAD ~ 4 # Undo the last four commits, keep changes
git reset --hard HEAD ~ 4  # Undo the last four commits, discard changes 
```

* Remove the file from Git without deleting it completely in git commit
You often add a file to the staging area ( git add ) that doesn’t belong there. 
You can use the command “ git rm “ here. However, this also removes the file from your file system.

However, if you want to keep the file in the filesystem, you can better remove it from the 
staging area with “git reset ”. Then add the file to the .gitignore so that you do not mistakenly 
pack it back into the staging index in the future. That’s how it’s done:

```bash
git reset Dateiname  # to reset the changes for a specific file Dateiname
echo Dateiname >> .gitignore # to avoid a file to be staged, we can add the file Dateiname in gitignore file.
```

* Git commit message change
git commit message changes Every programmer makes a typo on a commit. Fortunately, commit messages are very easy 
to correct using the “git commit — amend” command. you can commit your code with your own git commit with a message.
That’s how it’s done:

```bash
git commit --amend # Start the standard text editor to edit the commit message
git commit --amend -m "My new commit message"  # Sets the new message directly
```
