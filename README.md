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

---

## 🎯 Conclusion

This Git cheat sheet covers the essential commands you'll need for most workflows. Keep it handy as a quick reference guide, and enhance your Git skills with ease! If you need more advanced commands or explanations, don't hesitate to dive deeper into the Git documentation or explore additional resources.

---

This Markdown will render beautifully on GitHub and similar platforms, making your Git commands both functional and visually appealing in your `README.md` file.
