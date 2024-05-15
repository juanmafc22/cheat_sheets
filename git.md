# Git Cheat Sheet

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git status` | Check status | 
| `git config --global user.name "name"` | Set a name that is identifiable for credit when review version history |
| `git config --global user.email "email"` | Set an email address that will be associated with each history marker |
| `git config --list` | List all the configurations |
| `git branch -a` | List all the branches |
| `git branch <branch-name>` | Create a new branch |
| `git checkout <branch-name>` | Switch to a branch |
| `git branch -m <branch-name>` | Rename the current branch |
| `git branch -d <branch-name>` | Delete a branch |
| `git show` | Show the changes |
| `git remote -v` | List all the remote repositories |
| `git commit -m "message"` | Commit the changes |
| `git commit -am "message"` | Add and commit the changes |
| `git push -u origin <branch-name>` | Push the changes to the remote repository, and sets the upstrean branch, it establishes a tracking relationship |
| `git push` | Push the changes to the remote repository |
| `git pull` | Pull the changes from the remote repository |
| `git pull --rebase` | Pull the changes from the remote repository and rebase the changes |
| `git rebase --abort` | Abort the rebase done previously, and then just `git pull` |
| `git remote set-url origin <url>` | Change the remote repository URL |


