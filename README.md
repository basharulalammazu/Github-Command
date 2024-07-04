# Github-Command

## For First Time Push
**********************
```bash
git init   # Initialize a new Git repository in the current directory

git add README.md   # Stage the README.md file for commit

git add .   # Stage all other modified files for commit

git commit -m "Describe changes"  # Commit the staged changes with a descriptive message

git remote add origin <repository-url> # Add a remote repository named 'origin' with its URL

git remote -v  # Verify the remote repository URL (optional)

git push origin main  # Push the committed changes to the 'main' branch of the remote repository named 'origin'
```


## For Update Push
*****************
```bash
git add .   # Stage all modified files for commit

git commit -m "Describe changes"  # Commit the staged changes with a descriptive message

git push origin main/master  # Push changes to the 'main' or 'master' branch of the remote repository
```


## For Checking
***************
```bash
git status  # Check the status of the repository (optional)

git log  # View the commit history (optional)

git remote  # List configured remotes (optional)
```


## Force Push Changes (Use with Caution)
****************************************
```bash
git push -f  # Force push changes to the remote repository (use with caution)

git push -f -u origin main  # Force push changes to the 'main' branch of the remote repository 'origin'

git push origin master --force  # Another way to force push changes to the 'master' branch of the remote repository 'origin'
```


## Update Local Files from Remote Repository
********************************************
```bash
git stash  # Stash current changes in case of conflicts

git pull origin master  # Pull changes from the 'master' branch of the remote repository 'origin'

git stash apply  # Apply the stashed changes back to the working directory
```







