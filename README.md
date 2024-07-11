# Git Commands

## For First Time Push

| Command | Description |
| --- | --- |
| `git init` | Initialize a new Git repository in the current directory |
| `git add README.md` | Stage the README.md file for commit |
| `git add .` | Stage all other modified files for commit |
| `git commit -m "Describe changes"` | Commit the staged changes with a descriptive message |
| `git remote add origin <repository-url>` | Add a remote repository named 'origin' with its URL |
| `git push origin <branch name>` | Push the committed changes to the specified branch of the remote repository named 'origin' |

## For Update Push

| Command | Description |
| --- | --- |
| `git add .` | Stage all modified files for commit |
| `git commit -m "Describe changes"` | Commit the staged changes with a descriptive message |
| `git push origin <branch name>` | Push changes to the specified branch of the remote repository |

## For .gitignore File

| Command          | Description                        |
|------------------|------------------------------------|
| `nano .gitignore` | Create or edit the .gitignore file |
| `Ctrl + x`       | Save                               |
| `Ctrl + Y`       | Exit                               |
| `Enter`          | Confirm                            |
| `echo "*.log" >> .gitignore` | Add a new pattern to the .gitignore file |
| `git rm -r --cached .` | Remove all files from the Git index and re-add them to respect the .gitignore rules |
| `git add .gitignore` | Stage the .gitignore file for commit |
| `git commit -m "Update .gitignore"` | Commit the changes to the .gitignore file |
| `git rm -r --cached node_modules/` | Remove ignored files or directories from the repository |

## Navigating and Viewing Repository

| Command                           | Description                             |
|-----------------------------------|-----------------------------------------|
| `cd path/to/your/repository`      | Change directory to your repository     |
| `git remote -v` | Verify the remote repository URL (optional) |
| `git status` | Check the status of the repository (optional) |
| `git log` | View the commit history (optional) |
| `git remote` | List configured remotes (optional) |
| `git clone <repository-url>` | Clone the repository locally |

## Force Push Changes (Use with Caution)

| Command | Description |
| --- | --- |
| `git push -f` | Force push changes to the remote repository (use with caution) |
| `git push -f -u origin <branch name>` | Force push changes to the 'main' branch of the remote repository 'origin' |
| `git push origin <branch name> --force` | Another way to force push changes to the 'master' branch of the remote repository 'origin' |

## Update Local Files from Remote Repository

| Command | Description |
| --- | --- |
| `git stash` | Stash current changes in case of conflicts |
| `git pull origin <branch name>` | Pull changes from the 'master' branch of the remote repository 'origin' |
| `git stash apply` | Apply the stashed changes back to the working directory |


## Handling Large Files with Git LFS
| Command	| Description |
| --- | --- |
| `git lfs install` |	Initialize Git LFS in the repository |
| `git lfs track "*.<file type>"` |	Track all files of the specified type (e.g., .mp4, .gif) with Git LFS |
| `git add .gitattributes` |	Stage the .gitattributes file for commit |
| `git add .`	| Stage all other files for commit |
| `git commit -m "Describe changes"` |	Commit the staged changes with a descriptive message |
| `git push origin main` |	Push the committed changes to the 'main' branch of the remote repository |

## Branch Management

| Command | Description |
| --- | --- |
| `git branch` | List all local branches |
| `git branch <branch-name>` | Create a new branch |
| `git checkout <branch-name>` | Switch to the specified branch |
| `git checkout -b <branch-name>` | Create and switch to a new branch |
| `git branch -d <branch-name>` | Delete the specified branch |
| `git push origin --delete <branch-name>` | Delete the specified branch on the remote repository |
| `git branch --set-upstream-to origin main` | Set the upstream branch for the current local branch to `main` on the remote repository `origin` |

## Merging and Rebasing

| Command | Description |
| --- | --- |
| `git merge <branch-name>` | Merge the specified branch into the current branch |
| `git rebase <branch-name>` | Rebase the current branch onto the specified branch |
| `git rebase --continue` | Continue the rebase after resolving conflicts |
| `git rebase --abort` | Abort the rebase process |

## Viewing and Comparing Changes

| Command | Description |
| --- | --- |
| `git diff` | Show changes between working directory and the index |
| `git diff <branch-name>` | Show changes between working directory and the specified branch |
| `git diff <commit-id>` | Show changes between working directory and the specified commit |
| `git show <commit-id>` | Show details of the specified commit |

## Undoing Changes

| Command | Description |
| --- | --- |
| `git reset <file>` | Unstage the specified file |
| `git reset --hard` | Discard all changes in the working directory |
| `git revert <commit-id>` | Revert the specified commit |

## Tagging

| Command | Description |
| --- | --- |
| `git tag` | List all tags |
| `git tag -a <tag-name> -m "Tag message"` | Create an annotated tag |
| `git push origin <tag-name>` | Push the specified tag to the remote repository |
| `git push origin --tags` | Push all tags to the remote repository |

## Stashing Changes

| Command | Description |
| --- | --- |
| `git stash save "Your stash message"` | Save your changes to a stash with a message |
| `git stash list` | List all stashed changes |
| `git stash pop` | Apply the most recent stash and remove it from the stash list |
| `git stash apply stash@{2}` | Apply a specific stash without removing it from the stash list |
| `git stash drop stash@{0}` | Remove a specific stash from the stash list |
| `git stash clear` | Remove all stashes |

## Cherry-Picking Commits

| Command | Description |
| --- | --- |
| `git cherry-pick <commit-id>` | Apply the changes from a specific commit onto the current branch |

## Squashing Commits

| Command | Description |
| --- | --- |
| `git rebase -i HEAD~n` | Interactively rebase the last n commits to squash them |
| `# Follow the interactive rebase instructions in the editor` | Follow the interactive rebase instructions in the editor |

## Rewriting Commit History

| Command | Description |
| --- | --- |
| `git commit --amend -m "New commit message"` | Amend the most recent commit with a new message |
| `git rebase -i <commit-id>^` | Interactively rebase to rewrite commit history starting from a specific commit |
| `# Follow the interactive rebase instructions in the editor` | Follow the interactive rebase instructions in the editor |

## Restoring Files

| Command | Description |
| --- | --- |
| `git restore <file>` | Restore a specific file from the working directory |
| `git restore --staged <file>` | Unstage a specific file |

## Viewing Blame

| Command | Description |
| --- | --- |
| `git blame <file>` | Show who changed each line in a file |

## Configuring Git

| Command | Description |
| --- | --- |
| `git config --global user.name "Your Name"` | Set the global username for Git |
| `git config --global user.email "you@example.com"` | Set the global email for Git |
| `git config --global core.editor "code --wait"` | Set the default editor for Git |

## Creating and Applying Patches

| Command | Description |
| --- | --- |
| `git format-patch -1 <commit-id>` | Create a patch file for a specific commit |
| `git am <patch-file>` | Apply a patch file to the current branch |

## Aliases

| Command | Description |
| --- | --- |
| `git config --global alias.st status` | Create a shorthand alias for git status |
| `git config --global alias.co checkout` | Create a shorthand alias for git checkout |
| `git config --global alias.ci commit` | Create a shorthand alias for git commit |
| `git config --global alias.br branch` | Create a shorthand alias for git branch |
