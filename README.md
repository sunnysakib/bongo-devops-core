# Git & GitHub Mastery Assignment

This repository contains practical implementations and workflows covering fundamental to advanced Git operations completed as part of the DevOps & Cloud Engineering curriculum on bongoDev.

---

## 📌 Tasks Overview

| Task | Module / Topic | Key Git Commands Used | Summary |
| :--- | :--- | :--- | :--- |
| **01** | The Setup (Identity) | `git config`, `git init` | Configured global user credentials and initialized a new local repository. |
| **02** | First Commit (Checkpoint) | `git add`, `git commit` | Staged project files and created the initial repository checkpoint. |
| **03** | Parallel Universe (Branching) | `git checkout -b`, `git branch` | Created a feature branch to work on system optimizations without affecting `main`. |
| **04** | Time Machine (Checkout/Reset) | `git log`, `git checkout` | Navigated past commit history and learned how to undo uncommitted changes. |
| **05** | Cloud Connection (GitHub) | `git remote add`, `git push` | Connected the local repository to GitHub remote servers and pushed commit history online. |
| **06** | History Detective (Investigation) | `git blame`, `git log -p`, `git show` | Investigated file modifications to trace specific commit authors, timestamps, and hashes. |
| **07** | Safety Net (Context Switching) | `git stash`, `git stash pop` | Shelved uncommitted working changes temporarily to resolve an urgent hotfix on another file. |
| **08** | Clean Merge (Squash Workflow) | `git merge --squash` | Merged a feature branch into `main` while squashing multiple small commits into a single clean commit. |
| **09** | Conflict Resolution (Communication) | `git merge`, manual edit | Triggered a line-by-line conflict between two branches and manually resolved conflict markers. |
| **10** | Time Machine (Reflog Recovery) | `git reflog`, `git reset --hard` | Recovered a lost commit that was wiped via a hard reset by reading reference logs (`reflog`). |

---

## 🛠️ Detailed Git Commands Reference & Explanations

### **1. Setup & Initialization**
* `git config --global user.name "Your Name"`  
  **Why it's used:** Sets your identity name globally so Git tags your commits with your name.
* `git config --global user.email "your.email@example.com"`  
  **Why it's used:** Associates your email address with your commits to link them properly on remote hosts like GitHub.
* `git init`  
  **Why it's used:** Initializes a brand-new `.git` hidden repository directory inside your working folder to start tracking changes.

### **2. Staging & Basic Commits**
* `git add <file>` / `git add .`  
  **Why it's used:** Moves untracked or modified files from the working directory to the **Staging Area** (index) to prepare them for a snapshot.
* `git commit -m "commit message"`  
  **Why it's used:** Saves a permanent snapshot of all currently staged files into the local Git database with a descriptive summary.
* `git status`  
  **Why it's used:** Displays the current state of the working directory and staging area (shows modified, staged, or untracked files).

### **3. Branching & Context Switching**
* `git branch`  
  **Why it's used:** Lists all local branches in your repository and highlights the active branch.
* `git checkout -b <branch_name>` *(or `git switch -c <branch_name>`)*  
  **Why it's used:** Simultaneously creates a new branch and switches your active working environment to it.
* `git checkout <branch_name>` *(or `git switch <branch_name>`)*  
  **Why it's used:** Switches your working directory to an existing branch.

### **4. Stash (Temporary Storage)**
* `git stash`  
  **Why it's used:** Temporarily saves (shelves) uncommitted local changes and resets your working directory to a clean state so you can change tasks without committing incomplete code.
* `git stash pop`  
  **Why it's used:** Restores the most recently stashed changes back into your working directory and deletes them from the stash stack.

### **5. Merging & History Management**
* `git merge <branch_name>`  
  **Why it's used:** Joins history from the specified feature branch into your current active branch (`main`).
* `git merge --squash <branch_name>`  
  **Why it's used:** Combines all changes from a feature branch into a single staged change on your target branch, allowing you to create one clean, combined commit instead of cluttering history with multiple smaller commits.

### **6. History Inspection & Forensic Investigation**
* `git log` / `git log --oneline`  
  **Why it's used:** Displays the chronological commit history of the repository (author, date, hash, message). `--oneline` formats each commit into a compact line.
* `git blame <filename>`  
  **Why it's used:** Annotates each line of a file with the author, date, and commit hash responsible for writing or last modifying that line.
* `git log -p <filename>`  
  **Why it's used:** Shows the detailed line-by-line patch (diff) history for a specific file across all commits.
* `git show <commit_hash>`  
  **Why it's used:** Shows full details and diffs associated with one specific commit hash.

### **7. Recovery & Undoing Changes**
* `git reset --hard <commit_hash>`  
  **Why it's used:** Forcefully resets the active branch head, staging area, and working directory back to a specific past commit, discarding all uncommitted changes and subsequent commits.
* `git reflog`  
  **Why it's used:** Logs every position change of `HEAD` across all actions (commits, resets, checkouts). It serves as an undo mechanism to locate and restore accidentally deleted commits.

### **8. Remote Repository Operations**
* `git remote add origin <URL>`  
  **Why it's used:** Connects your local Git repository to a remote server endpoint (e.g., GitHub).
* `git branch -M main`  
  **Why it's used:** Renames the default local branch to `main`.
* `git push -u origin main`  
  **Why it's used:** Uploads local `main` branch commits to the remote `origin` repository on GitHub and sets `origin/main` as the default tracking branch.

---

## 🚀 Getting Started

To clone and inspect this repository locally:

```bash
git clone <YOUR_GITHUB_REPOSITORY_URL>
cd <REPOSITORY_FOLDER>
git log --oneline --graph --all
