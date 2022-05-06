# Git
    Git is version control system. lets begin basics.
    Create Github account and install git in machine.
    
### git clone
    Helps to clone remote repository to local machine.
    command syntax
    git clone <path>
    ex:
    git clone https://github.com/Harinath13693/test.git

### git config
    Helps to configure user details. 
    
    command syntax to configure email
    git config --global user.email "mailaddress"
    ex:
    git config --global user.email "harinath13693@gmail.com"
    
    command syntax to configure username
    git config --global user.name "username"
    ex:
    git config --global user.name "harinath13693"
    
### git add
    Helps to add changes made working area to stage area
    To add single file.
    git add <file name>
    
    To add all files
    git add -A
    
    To add all files in the directory 
    git add .
    
    To add add changes line by line
    git add -P
    
### git commit
    Helps to move from stage area to local repository
    To commit all files
    git commit -m 'message'
    
    To commit single file 
    git commit 'filename' -m 'commit message'
    ex:
    git commit 'git_commands.txt' -m 'commiting single file'
    
    To add and commit multiple file from stage Area
    git commit -am 'commit message' 
    ex:
    git commit -am 'adding commiting multiple files'
    
    To add and commit single file from stage Area
    git commit <filename> -m 'commit message' 
    ex:
    git commit 'revision.txt' -m 'adding commiting single file'
    
    To amend(change) the commit message for previous commit
    git commit -amend 'changed commit message'
    ex:
    git commit --amend 'single file'
    
### git reset/restore/checkout
    Helps to reset at various levels
    
    To discard changes in working directory
      single file
      $ git checkout -- <filename>
      $ git restore <filename>
      ex:
      $ git restore revision.txt
    
      Multiple files 
      $ git restore .
      $ git checkout -- .
      
      To Remove new files
      $ git clean -f
      
    To move back changes from staging area to working directory
    git reset head
    git restore --staged <filename>
    ex:
    git restore --staged revision.txt
    
    To discard changes from staging area
    git reset --hard
    
    To move changes local repoistory to staging area
    git reset --soft head~1
    
    To discard changes from local repository 
    git reset --hard head~1
    
    To move back to specfic commit
    git reset 'commit code'
       --it deletes permanently all the commites after  mentioned commit
    git revert 'commit code'
       --it creates one more commit with all previous history of commits
       
### git log
    Helps to show history of commits
    git log
    
    git reflog
    
### git branch
    Branches helps to maintain versions, different environments.
    git branch
        --displays all branches 
    git branch -r
        --displays all branches on remote repository
    git branch -a
        --displays all branches on local repository
    git checkout <branch_name>
        --switches to specified branch_name
    git checkout -b <branch_name>
    git branch <branch_name>
        --creates new branch with the specifed name on local repository
    git push --set-upstream origin <branch_name>
        -- pushes new branch to remote repository
    git checkout -d <branch_name>
        -- Deletes branch on local repository
    git push origin --delete  <branch_name>
        -- deletes branch on remote repository
        
 ### git push
    Helps push commit local repo to remote repo
    git push
    git push -all origin
        -- pushes all commits in all branches
    git push <branch_name>
    git push origin <branch_name>
        -- pushes only specifed branch changes to remote repo
        
### git fetch
    Helps to fetch latest version remote repo to local repo but not merges
    git fetch
    
### git merge
    Helps to merge code between branches and diff versions of same branch
    git merge branch_name1 branch_name2
        --merges branch_name2 in branch_name1
    git merge other_branch
        --merges other_branch in current branch
          While mergeing can occur conflicts.
          whenever merge conflicts occurs need to reslove by choosing specfic changes or new changes
          
### git pull
    Helps to fectch data from remote repo and merge in local repo and working directory
    git pull
    git pull=git fetch + git merge
    
### head/difftool
        head refers most recent commit
        git show head
            --shows recent commit
        git show head~1 head
            -- shows changes between most recent commit and before that
        git difftool head~1 head
            -- shows difference between each file with previous commit 

### git stash
    Whenever we switch between branches, working tree has to be clean, which means all changes has to be committed or discarded.
    If not switching is not allowed, we have to switch forcefully and changes are discarded.
    Here comes git stash which helps to save changes locally and can use later.
    we can stash more than 1 time, will store as stack
    git checkout -f <branch name>
        --switching branches forcefully
    git stash
        -- stashes without a name and comment
     git stash save 'message'
        -- stash with a name
     git stash pop 
        -- most recent stash stack changes will pop into working directory and deletes in stack
     git stash pop stash@{n}
        -- specified stash is poped and deleted in stash stack
     git stash apply
        -- it apply recent(top) stash stack and will not deleted in the stack
     git stash apply stash@{n}
        -- speficed stash is applied and stash stack is not deleted
     git stash clear
        --deletes all stash stack
     git stash drop stash@{n}
        --deletes n specified stash
     git stash show stash@{n}
        -- shows difference between current commit and stash changes
     git stash branch <new_branch_name> stash@{n}
        -- creates new branch new_branch_name and add all changes os stash of specified number.
        
     
      
    
    
    
    
