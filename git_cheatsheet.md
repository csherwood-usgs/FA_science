### Git cheat sheet - the commands you need once it is installed

(Note...whenever you see `<brackets>` in these notes, replace the text and the brackets with your info.)  

Remember, you need to run these commands inside the folder containing your local copy of the repo.  

You can confirm you are in a folder with a repo if you type `ls -a` and see a "hidden" folder called `.git`.  

The workflow is this:

`cd <folder with repo>` **before** you start work. 

`git pull` will update your local repo with any changes from the *origin* Github repo in the cloud.

`git add <filename>` will add the file to your local repo to be tracked.  

`git commit -a -m "<notes on these changes>"` will update your local repo with any changes.

`git push` will copy local changes up to the *origin* Github repo.  


#### Other commands

`git status`- just a check. It will probably report something like this:
```
On branch main
Your branch is up to date with 'origin/main'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        .ipynb_checkpoints/

nothing added to commit but untracked files present (use "git add" to track)
```
The .ipynb_checkpoints folder is changed by Jupyter lab, and is nothing to worry about.  

However, if you see an untracked file that you want to include in the repo, you need to `git add <that filename>`
