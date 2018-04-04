# Git Commands 1:

### Basic Git commands:

* __git init:__ Initialise git for that directory and all children. Be careful not to do this at a very hight level. It it normal to have 1 repo per project.

* __git status:__ Shows git status (branch), commit status, file tracking etc.

* __git add:__ Add files to the STAGING AREA. We need to add files before each commit. We are slecting what we want to commit at this point in time. To select all files we type ' . '

* __git commit:__ Effectively saves changes. Use the -m flag means we can add a message to our commit. Commit messages are written in the present tense.

* __git log:__ Shows a history / log of commits within this repo. Press 'q' to exit.

* __git checkout:__ Allows us to go back to previous commits. Git checkout 'hashedrefcode' allows us to go back to the hash ref and look at code. Git checkout master takes us back to master (most recent).

Most devs don't know how to revert to old commits off the top of their head. There are multiple ways of doing this, and opinion is divided on how it's done. We are using:

* __git revert__ The syntax for this is: git revert --no-commit _hashed code_..HEAD. This will revert everything from the HEAD back to the commit hash, meaning it will recreate that commit state in the working tree as if every commit since had been walked back. You can then commit the current tree, and it will create a brand new commit essentially equivalent to the commit you "reverted" to.

(The --no-commit flag lets git revert all the commits at once- otherwise you'll be prompted for a message for each commit in the range, littering your history with unnecessary new commits.)

This is a safe and easy way to rollback to a previous state. No history is destroyed, so it can be used for commits that have already been made public. See [here](https://stackoverflow.com/questions/4114095/how-to-revert-git-repository-to-a-previous-commit/21718540#21718540 "stackoverflow") for more info.

### More advanced Git commands:

* __Add multiple files of the same type:__ git add *.html

* __Add all files in directory (including hidden):__ git add -A

* __Removing files from staging area:__ git reset HEAD <filename> 

* __Ignoring files:__ make a file called .gitignore. Add names of files to be ignored.



    

