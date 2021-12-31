### First-Time Git Setup

```
git config --global user.name "Nguyen Ngoc Binh"
git config --global user.email nguyenngocbinhneu@gmail.com
```

### Delete branch local and remote
```{}
$ git push -d <remote_name> <branch_name>
$ git branch -d <branch_name>
```

### Renaming local and remote
```{}
# Rename the local branch to the new name
git branch -m <old_name> <new_name>

# Delete the old branch on remote - where <remote> is, for example, origin
git push <remote> --delete <old_name>

# Or shorter way to delete remote branch [:]
git push <remote> :<old_name>

# Prevent git from using the old name when pushing in the next step.
# Otherwise, git will use the old upstream name instead of <new_name>.
git branch --unset-upstream <old_name>

# Push the new branch to remote
git push <remote> <new_name>

# Reset the upstream branch for the new_name local branch
git push <remote> -u <new_name>
```
