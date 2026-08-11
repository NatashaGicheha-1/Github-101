<img width="736" height="1104" alt="image" src="https://github.com/user-attachments/assets/e745524f-1c45-43a8-ac9f-f8cee236b465" />

# Skills I have gained on Github so far 
## 1. Using Mau Forest Loss Data Analysis Repository
* Writing sentences in point form using *space
* Creating repositories
* Creating folders and pushing files in repositories.
* Connecting R project to Github repository.
* Making changes to an R file already in my repository.
* Version Control with Git:
    * git status – I checked whether file Analysis.R had changed and needed to be saved to Git before uploading to GitHub.
    * git add – I staged my project file Analysis.R so Git could include it in the next commit.
    * git commit – You created a saved checkpoint of your work with the message "Changing my main repository".
    * *git push* – I uploaded my local project changes from my computer to the GitHub repository Mau-Forest-Loss-Data-Analysis.
    * git pull – When GitHub had changes that were not on my computer, I downloaded those changes first so that my git push would not overwrite them.
    * git remote -v – I checked if my R project was correctly connected to the GitHub repository NatashaGicheha-1/Mau-Forest-Loss-Data-Analysis.
    * Resolving a push rejection (fetch first) – When GitHub rejected my push because the online repository had newer changes, I fixed the issue by pulling the latest version before pushing again.
    * GitHub authentication with multiple accounts – I discovered Git was using my previous GitHub account natashawanjiru181stack, removed the saved credentials, and authenticated with the correct account NatashaGicheha-1 that owns the repository.

## 2. Using Movie Recommendation System Repository
* Creating tables using |-----|------|
  
# Challenges I have Encountered Using Github and how I solved them
| # | Challenge Experienced | Cause | Solution Applied | Outcome |
|---|----------------------|---------|------------------|---------|
| 1 | Cloned a GitHub repository but could not find it afterward | Selected **"Open somewhere else"** instead of **"Open in Current Workspace"** during cloning | Searched for the repository and identified the folder being used in VS Code | Located the repository and understood where Git was operating |
| 2 | `git status` returned *"fatal: not a git repository"* | The folder being used was not initialized as a Git repository | Ran `git init` in the intended project folder | Successfully created a Git repository |
| 3 | VS Code terminal appeared to overwrite the path when typing | Terminal was behaving unexpectedly, causing confusion about where to type commands | Opened a fresh terminal and entered commands after the prompt (`>`) | Successfully executed Git commands |
| 4 | Created a new Git repository while another repository already existed | Repository location confusion during setup | Investigated `.git` folders and repository structure | Determined which repository should be retained |
| 5 | VS Code displayed two repositories simultaneously | A Git repository existed inside another Git repository (nested repositories) | Searched for all `.git` folders using PowerShell | Identified the nested repository causing the problem |
| 6 | Multiple `.git` folders created repository conflicts | One repository had been initialized inside another project folder | Removed the unnecessary nested repository manually | Left only the intended repository structure |
| 7 | Local commits were not appearing on GitHub | Repository was not connected to any remote repository | Checked remotes using `git remote -v` | Confirmed that no remote was configured |
| 8 | VS Code displayed **Publish Branch** instead of **Sync Changes** | No GitHub remote existed for the repository | Connected the repository using `git remote add origin <repository-url>` | Repository became linked to GitHub |
| 9 | GitHub repository and local repository showed different content | Local repository was disconnected and had a different commit history | Verified repository URL and reconnected the correct GitHub repository | Local and remote repositories became linked |
| 10 | GitHub contained a `main` branch while local repository used `master` | New repository initialization used `master`, while GitHub defaulted to `main` | Fetched GitHub changes and prepared to merge branch histories | Enabled consolidation of project history |
| 11 | GitHub reported that `main` and `master` had entirely different commit histories | Local repository and GitHub repository were created independently | Used `--allow-unrelated-histories` during merge | Allowed merge of both branch histories |
| 12 | Merge opened an editor and appeared to freeze | Git was waiting for a merge commit message to be saved | Saved and exited the merge message editor using `:wq` | Merge process completed successfully |
| 13 | Local work was on `master` but preferred workflow was `main` | Branch naming inconsistency | Switched to `main`, merged `master`, and prepared to push | Standardized development on the `main` branch |
| 14 | Unsure whether GitHub had received the latest changes | Branch synchronization uncertainty | Verified remotes, commits, branches, and push status | Confirmed repository state before publishing |
| 15 | Repository structure became confusing after multiple Git operations | Cloning, initializing, deleting repositories, and reconnecting remotes created mixed states | Systematically inspected `.git` folders, branches, and remotes | Restored a clean repository structure |

---

# Key Git Commands Used During Troubleshooting
### Initialize a repository

```bash
git init
```

### Check connected GitHub repositories

```bash
git remote -v
```

### Connect repository to GitHub

```bash
git remote add origin https://github.com/USERNAME/REPOSITORY.git
```



### Switch to the main branch

```bash
git checkout main
```

### Create a local main branch from GitHub

```bash
git checkout -b main origin/main
```

### Merge master into main

```bash
git merge master --allow-unrelated-histories
```

### Find all Git repositories

```powershell
Get-ChildItem -Recurse -Directory -Force -Filter ".git" | ForEach-Object { $_.FullName }
```

---

