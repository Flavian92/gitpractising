# gitpractising
learning git

git accaunt
git config --global user.name "Flavian"
git config --global user.email "flavian@libero.com"

Initialise directory:
1 navigate directory 
2 git init

exercise 1

navigate to a directory or create a folder mkdir gitpractising-1
git init  to initialise git in the directory
1. create a new repository

2. create a new file, add it to the index and commit it

touch myfile.txt  # Create a new file
git add myfile.txt  # Add the file to the index
git commit -m "Initial commit"  # Commit the file

3. launch gitk to display it. Keep the window open and hit F5 after each
command (to visualise the results of your commands)
gitk &

4. modify the file and make a new commit

# Edit myfile.txt using a text editor
git add myfile.txt
git commit -m "Modified myfile.txt"

5. rename the file (either with git mv or git add+git rm), do a git status
before committing (to ensure the renaming is correctly handled)

git mv myfile.txt newfile.txt
git status  # Check if the renaming is correctly handled
git commit -m "Renamed myfile.txt to newfile.txt"

6. delete the file and commit it

git rm newfile.txt
git commit -m "Deleted newfile.txt"

7. create two new files and commit them. Then modify their content in the
working copy and display the changes with git diff

touch file1.txt file2.txt
git add file1.txt file2.txt
git commit -m "Added file1.txt and file2.txt"
# Modify the content of file1.txt and file2.txt
git diff

8. add one file into the index but keep the other one. Display the changes
between:
• the index and the working copy
• the last commit and the index
• the last commit and the working copy

git add file1.txt  # Add file1.txt to the index
git diff  # View changes between the working copy and index
git diff --staged  # View changes between the last commit and the index
git diff HEAD  # View changes between the last commit and the working copy

9. run git reset to reset the index

git reset

10. run git reset --hard to reset the index and the working copy

git reset --hard


//more git 
show → show the details of a commit (metadata + diff)

git show 
commit 1d0dec96ba8b9541805c618f43ed19cf87d05242 (HEAD -> main, origin/main, origin/HEAD)
Author: Flavian92 <flavian>
Date:   Mon Oct 30 14:07:22 2023 +0100

    mod fileprova

diff --git a/fileprova.txt b/fileprova.txt
index b00ce13..70c379b 100644
--- a/fileprova.txt
+++ b/fileprova.txt
@@ -1 +1 @@
-hi^^^
\ No newline at end of file
+Hello world
\ No newline at end of file


 git log  show the history
commit 1d0dec96ba8b9541805c618f43ed19cf87d05242 (HEAD -> main, origin/main, origin/HEAD)
Author: Flavian92 <flavian
Date:   Mon Oct 30 14:07:22 2023 +0100

    mod fileprova

commit 70005a59ecbade5b231902f018ae45c0f5206af5
Author: Flavian92 <flavian
Date:   Mon Oct 30 13:58:24 2023 +0100

    14:00

commit d4e0ccd80523f2d9675b7f9a5929b11a05c02595
Author: Flavian92 <flavian
Date:   Mon Oct 30 13:48:15 2023 +0100


Creating a new branch
git checkout -b new branch [ starting point ]
 git status
On branch main
Your branch is up to date with 'origin/main'.

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\zefif\OneDrive\DEVOPS\02Git\startergit\gitpractising-1> git checkout -b development
Switched to a new branch 'development'
PS C:\Users\zefif\OneDrive\DEVOPS\02Git\startergit\gitpractising-1> git status
On branch development
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")


Switching between branches
git checkout [-m] branch name
 git checkout -m main  
Switched to branch 'main'
M       README.md
Your branch is up to date with 'origin/main'.
