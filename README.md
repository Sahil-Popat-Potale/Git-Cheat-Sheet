---

# 📄 Git Cheat Sheet

A comprehensive and easy-to-use Git cheat sheet to help you quickly reference the most common Git commands. Each command is accompanied by a brief description and an example, making it perfect for both beginners and experienced developers.

---

## 🛠️ Git Configuration

### **Set Global Username and Email**
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### **List All Configurations**
```bash
git config --list
```

---

## 📂 Repository Setup

### **Initialize a New Repository**
```bash
git init
```

### **Clone an Existing Repository**
```bash
git clone https://github.com/username/repository.git
```

---

## 🔄 Basic Workflow

### **Check the Status of Your Repository**
```bash
git status
```

### **Add Files to the Staging Area**
```bash
# Add a specific file
git add filename.txt

# Add all changes
git add .
```

### **Commit Changes**
```bash
git commit -m "Your commit message"
```

### **Push Changes to the Remote Repository**
```bash
git push origin main
```

### **Pull Changes from the Remote Repository**
```bash
git pull origin main
```

---

## 🌳 Branching

### **List All Branches**
```bash
git branch
```

### **Create a New Branch**
```bash
git branch new-branch
```

### **Switch to a Branch**
```bash
git checkout branch-name
```

### **Create and Switch to a New Branch**
```bash
git checkout -b new-branch
```

### **Merge a Branch into the Current Branch**
```bash
git merge branch-name
```

### **Delete a Branch**
```bash
git branch -d branch-name
```

---

## 🌐 Remote Repositories

### **Add a Remote Repository**
```bash
git remote add origin https://github.com/username/repository.git
```

### **View All Remote Repositories**
```bash
git remote -v
```

### **Remove a Remote Repository**
```bash
git remote remove origin
```

---

## 🕒 Logs and History

### **View the Commit History**
```bash
git log
```

### **View a Simplified Commit History**
```bash
git log --oneline
```

### **Show Differences Between Commits or Branches**
```bash
# Show differences between working directory and staging area
git diff

# Show differences between two branches
git diff branch1 branch2
```

---

## 💾 Stashing

### **Stash Changes**
```bash
git stash
```

### **Apply Stashed Changes**
```bash
git stash apply
```

### **List All Stashes**
```bash
git stash list
```

### **Drop a Stash**
```bash
git stash drop
```

---

## 🔄 Undoing Changes

### **Unstage a File**
```bash
git reset HEAD filename.txt
```

### **Undo a Commit and Keep Changes**
```bash
git reset --soft commit_hash
```

### **Undo a Commit and Remove Changes**
```bash
git reset --hard commit_hash
```

### **Restore a Specific File**
```bash
git checkout -- filename.txt
```

---

## 🗑️ Removing Files

### **Remove a File and Stage the Deletion**
```bash
git rm filename.txt
```

### **Remove a File from Staging but Keep It Locally**
```bash
git rm --cached filename.txt
```

---

## 🏷️ Tagging

### **Create a Lightweight Tag**
```bash
git tag tag-name
```

### **Create an Annotated Tag**
```bash
git tag -a tag-name -m "Tag message"
```

### **Push Tags to the Remote Repository**
```bash
git push origin tag-name
```

---

## 🔄 Fetching and Rebasing

### **Fetch Changes from a Remote Repository**
```bash
git fetch origin
```

### **Reapply Commits on Top of Another Base Tip**
```bash
git rebase branch-name
```

### **Abort a Rebase in Progress**
```bash
git rebase --abort
```


Here are the remaining Git commands organized into proper categories and formatted to continue from the previous cheat sheet:

---

## 🖼️ Tagging and Version Control

### **Delete a Tag**
```bash
git tag -d tag-name
```
**How it works**: This command deletes a tag locally from your repository. The tag will still exist on the remote until you delete it there as well.

### **Push All Tags to the Remote Repository**
```bash
git push origin --tags
```
**How it works**: The `git push --tags` command pushes all local tags to the remote repository, making them available to everyone.

### **Delete a Tag from the Remote Repository**
```bash
git push origin --delete tag tag-name
```
**How it works**: This command removes a tag from the remote repository so that it is no longer available to others.

---

## 🧹 Cleaning Up

### **Remove Untracked Files**
```bash
git clean -f
```
**How it works**: The `git clean` command removes untracked files from the working directory, helping you clean up unnecessary files. Use `-f` to force the deletion.

### **Dry Run to See What Would Be Removed**
```bash
git clean -n
```
**How it works**: This command performs a dry run, showing you which untracked files would be deleted without actually deleting them.

---

## 🔀 Rewriting History

### **Amend the Last Commit**
```bash
git commit --amend -m "Updated commit message"
```
**How it works**: The `git commit --amend` command allows you to modify the most recent commit. You can change the commit message or add new changes.

### **Rebase Interactively**
```bash
git rebase -i commit_hash
```
**How it works**: This command opens an interactive rebase session, where you can modify, combine, or delete previous commits.

---

## 🕹️ Cherry-Picking

### **Apply a Specific Commit to the Current Branch**
```bash
git cherry-pick commit_hash
```
**How it works**: The `git cherry-pick` command allows you to apply changes from a specific commit on one branch to another branch.

---

## 🚨 Conflict Resolution

### **Show Conflicts After a Merge**
```bash
git status
```
**How it works**: After a merge conflict, running `git status` will show the files that have conflicts. You can then manually resolve them.

### **Mark Conflicts as Resolved**
```bash
git add filename.txt
```
**How it works**: After resolving conflicts in a file, add the file to the staging area with `git add` to mark it as resolved.

### **Continue After Resolving Conflicts**
```bash
git merge --continue
```
**How it works**: This command continues the merge process after you've resolved any conflicts.

### **Abort a Merge**
```bash
git merge --abort
```
**How it works**: This command aborts a merge in progress and returns the repository to its previous state before the merge started.

---

## ⚙️ Advanced Workflows

### **Squash Commits**
```bash
git rebase -i HEAD~n
```
**How it works**: The `git rebase -i` command lets you combine several commits into one. Replace `n` with the number of commits you'd like to squash.

### **Bisect to Find Buggy Commits**
```bash
git bisect start
git bisect bad
git bisect good commit_hash
```
**How it works**: The `git bisect` command performs a binary search to find which commit introduced a bug. Mark the bad and good commits, and Git will help you locate the culprit.

---

## 🔒 Security and Maintenance

### **Sign a Commit**
```bash
git commit -S -m "Signed commit message"
```
**How it works**: This command signs your commits with a GPG key, ensuring their authenticity and integrity.

### **Verify Signed Commits**
```bash
git log --show-signature
```
**How it works**: This command checks the signatures of past commits, confirming whether they were signed and valid.

---

## 📊 Git Aliases

### **Create a Git Alias**
```bash
git config --global alias.co checkout
```
**How it works**: The `git config` command lets you create shortcuts for frequently used Git commands. Here, `git co` becomes shorthand for `git checkout`.

### **List All Aliases**
```bash
git config --get-regexp alias
```
**How it works**: This command lists all your Git aliases, showing you the shortcuts you've set up for quicker workflows.

---

## 🗂️ Submodules

### **Add a Submodule**
```bash
git submodule add https://github.com/username/repository.git
```
**How it works**: The `git submodule add` command includes another Git repository as a submodule within your project, allowing you to track it as a separate module.

### **Initialize Submodules**
```bash
git submodule init
```
**How it works**: This command initializes all submodules in your project after they have been cloned.

### **Update Submodules**
```bash
git submodule update
```
**How it works**: The `git submodule update` command updates all submodules to their latest commits, ensuring they are in sync with the parent project.

---

## 🏗️ Hooks

### **Create a Pre-Commit Hook**
```bash
# Navigate to .git/hooks/ directory
cd .git/hooks/

# Create a new pre-commit hook
touch pre-commit
```
**How it works**: This command creates a pre-commit hook script in the `.git/hooks/` directory. Pre-commit hooks run before each commit to check code quality or perform other tasks.

---

## 🎯 Conclusion

This Git cheat sheet covers the essential commands you'll need for most workflows. Keep it handy as a quick reference guide, and enhance your Git skills with ease! If you need more advanced commands or explanations, don't hesitate to dive deeper into the Git documentation or explore additional resources.

---
