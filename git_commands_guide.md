
# 📘 Git Commands – Complete Guide

Git is a **distributed version control system** used to track changes in source code, collaborate with teams, and manage project history.  
This guide covers **all essential Git commands**, **how to use them**, and **when to use them**.

---

## 🔹 1. Git Configuration
Before using Git, configure your identity.

```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
git config --list
```
✅ **Use when** setting up Git for the first time. Ensures commits are linked to your identity.

---

## 🔹 2. Git Basics
```bash
git init        # Initialize a new Git repository
git clone <url> # Clone a remote repo
git status      # Check repo status
git help <cmd>  # Get help for a command
```
✅ **Use when** starting a new project, cloning an existing repo, or checking changes.

---

## 🔹 3. Working with Files
```bash
git add <file>      # Stage a file
git add .           # Stage all changes
git reset <file>    # Unstage a file
git rm <file>       # Remove file from repo
```
✅ **Use when** preparing changes before committing.

---

## 🔹 4. Committing Changes
```bash
git commit -m "Message"    # Commit with message
git commit -am "Message"   # Add & commit tracked files
```
✅ **Use when** saving staged changes with meaningful messages.

---

## 🔹 5. Branching
```bash
git branch                # List branches
git branch <name>         # Create new branch
git checkout <name>       # Switch branch
git checkout -b <name>    # Create & switch
git branch -d <name>      # Delete branch
```
✅ **Use when** working on features, bug fixes, or experiments.

---

## 🔹 6. Merging & Rebasing
```bash
git merge <branch>        # Merge branch into current
git rebase <branch>       # Reapply commits on top of another branch
git merge --abort         # Cancel merge
git rebase --abort        # Cancel rebase
```
✅ **Use when** combining branches or cleaning commit history.

---

## 🔹 7. Remote Repositories
```bash
git remote -v                   # List remotes
git remote add origin <url>     # Add remote repo
git push -u origin main         # Push to remote
git fetch origin                # Fetch latest changes
git pull origin main            # Pull latest changes
```
✅ **Use when** collaborating with remote repositories.

---

## 🔹 8. Stashing
```bash
git stash           # Save changes temporarily
git stash list      # View stashes
git stash apply     # Apply latest stash
git stash pop       # Apply & remove latest stash
```
✅ **Use when** switching tasks without committing changes.

---

## 🔹 9. Viewing History & Logs
```bash
git log                     # View commit history
git log --oneline --graph   # Simplified history
git diff                    # Show changes
git show <commit>           # Show commit details
```
✅ **Use when** tracking history, debugging, or reviewing changes.

---

## 🔹 10. Undoing Changes
```bash
git checkout -- <file>    # Discard local changes
git reset --soft <commit> # Reset staged changes (keep working files)
git reset --hard <commit> # Reset everything to commit
git revert <commit>       # Revert a commit
```
✅ **Use when** undoing mistakes or restoring repo state.

---

## 🔹 11. Tagging
```bash
git tag                  # List tags
git tag v1.0             # Create lightweight tag
git tag -a v1.0 -m "msg" # Annotated tag
git push origin v1.0     # Push tag
```
✅ **Use when** marking versions/releases.

---

## 🔹 12. Collaboration Workflow
1. `git clone` – Copy repo  
2. `git checkout -b feature-branch` – Create branch  
3. `git add . && git commit -m "Message"` – Stage & commit changes  
4. `git push origin feature-branch` – Push changes  
5. Create a **Pull Request** on GitHub/GitLab/Bitbucket.  

---

## 🔹 13. Advanced Commands
```bash
git cherry-pick <commit>   # Apply specific commit
git reflog                 # Show reference history
git blame <file>           # Show who changed each line
git bisect                 # Find buggy commit
```
✅ **Use when** debugging, tracing, or selectively applying changes.

---

## 📌 Conclusion
- **Manual Testing** ensures usability,  
- **Automation Testing** ensures speed.  
- Similarly, in Git, balance **committing small changes** vs **maintaining clean history**.  

🚀 Mastering these commands makes you efficient in **collaborative development** and **version control**.

---
