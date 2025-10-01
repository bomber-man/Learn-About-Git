# Git Interview Questions and Answers

This document provides **90 Git interview questions** with detailed answers, divided into three levels: Foundation, Proficient, and Advanced.

---

## 🟢 Foundation Level (Beginner)

### 1. What is Git?
Git is a **distributed version control system** that helps track changes in source code, allowing multiple developers to collaborate on projects efficiently. Unlike centralized systems, every developer has a complete local copy of the repository.

### 2. What is the difference between Git and GitHub?
- **Git**: A version control system to track code changes.
- **GitHub**: A cloud-based hosting service for Git repositories with collaboration features like pull requests, issue tracking, and CI/CD integration.

### 3. How do you check the current Git version?
```bash
git --version
```

### 4. What is a Git repository?
A Git repository is a **data structure that stores metadata and object database** for a project. It can be local (on your machine) or remote (on platforms like GitHub, GitLab, Bitbucket).

### 5. How do you initialize a new Git repository?
```bash
git init
```
This creates a new `.git` folder to track project changes.

### 6. How do you clone an existing Git repository?
```bash
git clone <repository_url>
```

### 7. What are Git branches?
Branches allow developers to **work on features independently**. The `main` (or `master`) branch is typically the default branch.

### 8. How do you create a new branch?
```bash
git branch <branch_name>
```

### 9. How do you switch to another branch?
```bash
git checkout <branch_name>
# or the modern command:
git switch <branch_name>
```

### 10. How do you create and switch to a branch in one step?
```bash
git checkout -b <branch_name>
# or
git switch -c <branch_name>
```

### 11. How do you check the status of files in Git?
```bash
git status
```

### 12. How do you add files to staging?
```bash
git add <file_name>
# or add all changes
git add .
```

### 13. How do you commit changes?
```bash
git commit -m "Commit message"
```

### 14. What is the difference between `git add` and `git commit`?
- `git add`: Moves changes to the **staging area**.
- `git commit`: Saves staged changes into the repository history.

### 15. How do you view commit history?
```bash
git log
```

### 16. How do you see a summarized version of commit history?
```bash
git log --oneline --graph --all
```

### 17. What is the difference between `git fetch` and `git pull`?
- `git fetch`: Downloads changes but does not merge them.
- `git pull`: Downloads and merges changes from remote into local.

### 18. How do you push changes to a remote repository?
```bash
git push origin <branch_name>
```

### 19. How do you configure username and email in Git?
```bash
git config --global user.name "Your Name"
git config --global user.email "your@email.com"
```

### 20. What is `.gitignore`?
A `.gitignore` file specifies **files and directories to be ignored** by Git, such as logs, build artifacts, or environment files.

### 21. How do you remove a file from Git but keep it locally?
```bash
git rm --cached <file>
```

### 22. What is `HEAD` in Git?
`HEAD` is a pointer that refers to the **latest commit in the currently checked-out branch**.

### 23. How do you rename a branch in Git?
```bash
git branch -m <old_name> <new_name>
```

### 24. How do you delete a branch?
```bash
git branch -d <branch_name>
# Force delete:
git branch -D <branch_name>
```

### 25. How do you see the difference between commits?
```bash
git diff
```

### 26. How do you unstage a file?
```bash
git reset <file>
```

### 27. How do you undo the last commit but keep changes?
```bash
git reset --soft HEAD~1
```

### 28. How do you discard local changes in a file?
```bash
git checkout -- <file>
```

### 29. How do you stash changes?
```bash
git stash
```

### 30. How do you apply the last stashed changes?
```bash
git stash apply
```

---

## 🟡 Proficient Level (Intermediate)

### 1. What is the difference between a fork and a branch?
- **Branch**: Exists within a repository for feature development.
- **Fork**: A complete copy of another repository (often used in open-source contributions).

### 2. What is the difference between `merge` and `rebase`?
- **Merge**: Creates a new merge commit, preserving history.
- **Rebase**: Moves commits on top of another branch, creating a linear history.

### 3. How do you resolve a merge conflict?
- Open conflicting files.
- Edit to resolve conflicts.
- Mark as resolved:
```bash
git add <file>
git commit
```

### 4. What is a detached HEAD state?
Occurs when `HEAD` points directly to a commit instead of a branch. Any new commits won’t belong to a branch.

### 5. How do you create an annotated tag?
```bash
git tag -a v1.0 -m "Version 1.0"
```

### 6. How do you list all tags?
```bash
git tag
```

### 7. How do you push a specific tag to remote?
```bash
git push origin <tag_name>
```

### 8. What is cherry-pick in Git?
`git cherry-pick <commit>` applies a specific commit from one branch to another.

### 9. How do you revert a commit?
```bash
git revert <commit_id>
```

### 10. Difference between `git reset` and `git revert`?
- **reset**: Moves HEAD to a specific commit (can alter history).
- **revert**: Creates a new commit that undoes changes.

### 11. What are Git hooks?
Scripts that run automatically on events (e.g., pre-commit, pre-push).

### 12. How do you squash multiple commits into one?
```bash
git rebase -i HEAD~n
```

### 13. How do you change the message of the last commit?
```bash
git commit --amend
```

### 14. How do you see which branches contain a specific commit?
```bash
git branch --contains <commit>
```

### 15. How do you remove untracked files?
```bash
git clean -f
```

### 16. How do you remove untracked directories as well?
```bash
git clean -fd
```

### 17. What is the difference between `origin` and `upstream`?
- **origin**: Default remote repository.
- **upstream**: Typically refers to the original repository from which a fork was made.

### 18. How do you track a remote branch?
```bash
git checkout --track origin/<branch>
```

### 19. How do you see remote URLs?
```bash
git remote -v
```

### 20. How do you change a remote repository URL?
```bash
git remote set-url origin <new_url>
```

### 21. How do you undo a merge commit?
```bash
git revert -m 1 <merge_commit_hash>
```

### 22. How do you move a commit to another branch?
```bash
git checkout <branch>
git cherry-pick <commit>
```

### 23. What is the reflog in Git?
`git reflog` shows a log of all HEAD movements, useful for recovering lost commits.

### 24. How do you see changes introduced by a commit?
```bash
git show <commit>
```

### 25. How do you bisect to find a bug?
```bash
git bisect start
git bisect bad
git bisect good <commit>
```

### 26. How do you archive a Git repository?
```bash
git archive --format=zip HEAD > repo.zip
```

### 27. What is the difference between shallow and full clone?
- **Shallow clone**: Limited commit history (`--depth=1`).
- **Full clone**: Complete history.

### 28. How do you list all branches (local and remote)?
```bash
git branch -a
```

### 29. How do you rename a remote branch?
- Rename locally:
```bash
git branch -m old_name new_name
```
- Delete old and push new:
```bash
git push origin :old_name new_name
```

### 30. How do you fetch and prune remote-tracking branches?
```bash
git fetch --prune
```

---

## 🔴 Advanced Level (Expert)

### 1. What is Git internals: objects, blobs, trees, and commits?
- **Blob**: Stores file content.
- **Tree**: Directory structure.
- **Commit**: Snapshot of the project with metadata.
- **Object database**: Stores everything in `.git/objects`.

### 2. What is the difference between SHA-1 and SHA-256 in Git?
Git originally used **SHA-1** for commit hashes, but newer versions support **SHA-256** to enhance security.

### 3. What is a bare repository?
A repository without a working directory, usually used on remote servers for collaboration.

### 4. How does Git store data internally?
Git stores everything as **objects (blobs, trees, commits)** in `.git/objects`, identified by their SHA hash.

### 5. What is the difference between `git rebase` and `git merge --squash`?
- **Rebase**: Rewrites commits on top of another branch.
- **Merge squash**: Combines multiple commits into one before merging.

### 6. How do you create a patch in Git?
```bash
git format-patch -1 <commit>
```

### 7. How do you apply a patch?
```bash
git apply <patch_file>
```

### 8. What are submodules in Git?
Submodules allow you to **include another Git repository inside a repository**.

### 9. How do you add a submodule?
```bash
git submodule add <repo_url>
```

### 10. How do you update submodules?
```bash
git submodule update --init --recursive
```

### 11. How do you remove a submodule?
- Remove from `.gitmodules`
- Run:
```bash
git rm --cached <submodule_path>
```

### 12. How do you split a repository into multiple ones?
Using:
```bash
git filter-repo
# or old method
git filter-branch
```

### 13. How do you combine multiple repositories into one?
Using `git remote add` and merging histories.

### 14. How do you optimize a Git repository?
```bash
git gc --aggressive --prune=now
```

### 15. What is Git LFS (Large File Storage)?
Extension for handling **large binary files** without bloating Git history.

### 16. How do you use Git LFS?
```bash
git lfs install
git lfs track "*.psd"
```

### 17. How do you sign commits in Git?
```bash
git commit -S -m "Signed commit"
```

### 18. How do you verify signed commits?
```bash
git log --show-signature
```

### 19. How do you find dangling commits?
```bash
git fsck --lost-found
```

### 20. How do you recover a deleted branch?
Find commit hash from reflog and recreate:
```bash
git checkout -b <branch> <commit_hash>
```

### 21. What is a worktree in Git?
`git worktree` allows multiple working directories attached to the same repository.

### 22. How do you create a new worktree?
```bash
git worktree add ../path branch_name
```

### 23. How do you use sparse checkout?
```bash
git sparse-checkout init
git sparse-checkout set <path>
```

### 24. What is a shallow clone with depth and single branch?
```bash
git clone --depth=1 --branch <branch> <url>
```

### 25. How do you find the author of a specific line?
```bash
git blame <file>
```

### 26. How do you benchmark Git performance?
Using:
```bash
git count-objects -vH
```

### 27. How do you use Git rerere (reuse recorded resolution)?
```bash
git config --global rerere.enabled true
```

### 28. How do you check for large files in history?
```bash
git rev-list --objects --all | sort -k 2 > allfiles.txt
```

### 29. How do you completely remove a file from history?
```bash
git filter-repo --path <file> --invert-paths
```

### 30. How do you handle monorepos in Git?
- Use sparse-checkout for performance.
- Use submodules or subtrees for modularity.
- CI/CD pipelines for partial builds.

---
