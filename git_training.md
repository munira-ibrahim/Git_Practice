# Fun Fact
- Staging area is same for all branch
- After resolving merge conflict 
    1. ctrl+s 
    2. commit code 
    3. merge
- After removing staged file locally 
    1. commit code 
    2. push to remote repo

# Bonus Command :
```
git add --all && git commit -m "Message"

git remote add origin <remote-repo-url>

git branch -M master main

git pull origin master --allow-unrelated-histories
```
# Commands : For Local Git Repository
```
git init
git --help
git add <filename>
git commit -m "Messege"
git status
git log
git ls-files - (List tracked/staged files)

```

# List Local & Remote Branch
```
git branch          - (List all local branches)
git branch -vv      - (List all local & remote branches mapping)

git branch -a       - (List all local & remote branches)
git ls-remote       - (List all remote branch)
```
 
# Create Branch
```
git branch <branchname>             - (create new branch)
git checkout -b <branchname>        - (create and access newly created branch)
git checkout/switch <branchname>    - (switch to branch)
git switch -c <branchname>          - (create branch)
```

# Git Merge
#### Fast Forward : (Add All commits from other branch- default merge) 
```
git merge <other-branch>    -(merge other branch with Current branch)
```

#### Squash Merge : (Add only one commit for all commit from other branch)
```
git merge --squash <Other-branch-name>
```

#### Recursive Merge:
```
git merge --no-ff <other-branch>
```


# Git Stash : Keep your work without committing/staging (you can go to 1 stash at a time)
```
git stash
git stash apply [index]
git stash list          - (list all stash)
git stash push          - (push stash item with message)
git stash pop           - (pop stash item)
git stash drop [index]  - (drop single stash item)
git stash clear         - (clear all stash history)
```

```
git reflog  - (All log of commits(Existing/deleted))
```

# Head :
- Last commit made on any branch called head.

# Can Delete Data :
### Remove File From Working Directory(commited/staged file)
```
git rm <file-name>
```

### From Current Commit:
```
git reset HEAD~1
```

### From previous commit:

### From Staged Area(delete staged content of file):
```
git reset <filename> 
        OR  
git restore --staged <filename>     - (This command will put modified data in unstaged area with below command)
git checkout -- <filename>          - (Remove Modified content from unstaged area) 
```

### From Unstaged Area(Unstaged Content):
```
git checkout .    
    OR 
git restore <file-name>
```

### Delete Untracked File:
```
git clean -df
```

### Delete Last Commit Locally & Remotely :
```
git reset --hard HEAD~1                 - (Locally)
git push --force origin <branch-name>   - (remote server)
```


### Branch(Delete branch) : 
```
git branch -D <branch-name> `           - (delete local branch)
git push origin --delete <branch-name>  - (delete remote branch)
```


# GitHub Command (For remote repository) :
- After Committing changes Locally use Following command to push to remote repository
```
git push -u origin <branch-name>  
        OR 
git push
```

### Map remote git hub branch to local tracking branch
```
git fetch                       - (fetch remote branch , git merge)
git branch --track <local-branch-name> origin/<remote-branch-name> - (map remote branch to local tracking branch)
        OR
git branch -u remote_name/branch_name local_branch_name
```

# Git Pull
- git pull = git fetch + git merge
```

git pull <remote-url> <branch-name>
git pull <remote-url> <branch-name> --force 
git pull origin <branch-name>
```

