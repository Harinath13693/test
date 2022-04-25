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

    
    
    
    
    
