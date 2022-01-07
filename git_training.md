# Fun fact:
>Staging area is same for all branch
>After resolving merge conflict 1)ctrl+s 2)commit code 3)merge
>After removing staged file locally 1)commit code 2)push to remote repo

# Commands : for Local git repository
>git init
>git --help
>git add <filename>
>git commit -m "Messege"
>git status
>git log
>git ls-files - List tracked/staged files

# List local and remote branch
>git branch - List all local branches
>git branch -vv :- List all local & remote branches mapping

>git branch -a  :- List all local & remote branches
>git ls-remote :- List all remote branch
 

>git branch <branchname> - create new branch
>git checkout -b <branchname> - create and access newly created branch
>git checkout/switch <branchname> - switch to branch
>git switch -c <branchname> - create branch

# git merge
: fast forward: (Add All commits from other branch- default merge)
>git merge <other-branch> - merge other branch with Current branch

: Squash merge : (Add only one commit for all commit from other branch)
> git merge --squash <Other-branch-name>

: Recursive merge:
> git merge --no-ff <other-branch>


# git stash : Keep your work without committing/staging (you can got to 1 stash at a time)
>git stash
>git stash apply [index]
>git stash list - list all stash
>git stash push - push stash item with message
>git stash pop - pop stash item
>git stash drop [index] - drop single stash item
>git stash clear - clear all stash history

>git reflog - All log of commits(Existing/deleted)

# Head :
>Last commit made on any branch called head.

### Can Delete data :
# Remove file from working directory(commited/staged file)
: git rm <file-name>

# from Current commit:
: git reset HEAD~1

# from previous commit:

# from staged area(delete staged content of file):
: git reset <filename> OR : git restore --staged <filename>- (This command will put modified data in unstaged area) with below command
:git checkout -- <filename> - (Remove Modified content from unstaged area) 

# from unstaged area(Unstaged Content):
: git checkout .    OR 
: git restore <file-name>

# Delete Untracked file:
: git clean -df

# delete Last commit locally and remotely :
: git reset --hard HEAD~1  - Locally
: git push --force origin <branch-name> - remote server


# branch(Delete branch) : 
: git branch -D <branch-name> - delete local branch
: git push origin --delete <branch-name> - delete remote branch


# GitHub Command (For remote repository) :
> After Committing changes Locally use Following command to push to remote repository
: git push -u origin <branch-name>  OR : git push

> [Map remote git hub branch to local tracking branch]
: git fetch : fetch remote branch , git merge
: git branch --track <local-branch-name> origin/<remote-branch-name> : map remote branch to local tracking branch.

# git pull
> git pull = git fetch + git merge
: git pull
: git pull origin <branch-name>

