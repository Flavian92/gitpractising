# gitpractising
learning git

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
