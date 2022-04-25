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
        -- pushes all co
    
        
        
    

    
    
    
    
    
