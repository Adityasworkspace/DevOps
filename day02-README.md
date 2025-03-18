DAY 02 
  
What is Git?
Git is a distributed version control system that tracks code changes and enables collaboration among developers. It allows you to commit, branch, merge, and revert code changes efficiently.

Key Git Concepts
  
Repository (Repo) – A directory containing your project and Git tracking files.
Commit – A snapshot of your project at a specific point in time.
Branch – A separate version of your code for independent development.
Merge – Combining changes from different branches.
Pull & Push – Syncing changes between your local and remote repositories.
Clone & Fork – Copying repositories for collaboration.



How to download and install the git ?  
  
🖥️ Windows Installation
  
Step 1: Download Git
Go to Git's official website.
Click on Windows to download the latest Git for Windows installer.
  
Step 2: Install Git
Run the downloaded .exe file.
Click Next and follow the setup wizard.
Choose Git Bash and Git GUI when prompted.
Select "Use Git from the Windows Command Prompt" (recommended).
Choose OpenSSH as the SSH client (default).
Select "Use the default branch name ‘main’".
Click Install and wait for the process to finish.
  
Step 3: Verify Installation
After installation, open Command Prompt (cmd) or Git Bash and type:
git --version
If Git is installed correctly, you’ll see the version number.
  


  
🐧 Linux Installation
  
Step 1: Install Git Using Terminal
Debian/Ubuntu:-
sudo apt update
sudo apt install git -y

Step 2: Verify Installation - 
git --version
You should see output like git version 2.x.x.
  

Commamds for using git:
 Step 1: Create/Edit the README.md File
Run the following command to create/edit a README.md file:

bash
Copy
Edit
echo "# Git Commands Cheat Sheet" > README.md && nano README.md
Then, paste the following content:

markdown
Copy
Edit
# 🚀 Git Commands Cheat Sheet

Git is a **version control system** that helps track changes in code. Below are various types of Git commands categorized by their functions.

---

## 📌 1. Basic Git Setup
```bash
git --version             # Check Git version
git config --global user.name "Your Name"   # Set username
git config --global user.email "your-email@example.com"  # Set email

📌 2. Repository Management
git init                  # Initialize a new Git repository
git clone <repo-URL>       # Clone a remote repository
git remote add origin <repo-URL>  # Link local repo to remote
git remote -v             # Show remote connections

📌 3. Staging & Committing Changes
git status                # Check status of working directory
git add <file>            # Add a specific file to staging
git add .                 # Add all files to staging
git commit -m "Your message"  # Commit changes with a message

📌 4. Branching & Merging
git branch                # List branches
git branch new-branch     # Create a new branch
git checkout new-branch   # Switch to new branch
git checkout -b new-branch  # Create & switch to new branch
git merge new-branch      # Merge new-branch into main
git branch -d new-branch  # Delete a branch

📌 5. Pushing & Pulling Changes
git push origin main      # Push changes to GitHub
git push -u origin main   # Push and set upstream branch
git pull origin main      # Pull latest changes from GitHub
git fetch                 # Fetch latest changes without merging

📌 6. Undo & Reset Changes
git reset --soft HEAD~1   # Undo last commit but keep changes
git reset --hard HEAD~1   # Undo last commit & delete changes
git revert <commit-hash>  # Revert a specific commit

📌 7. Viewing History & Logs
git log                   # Show commit history
git log --oneline --graph --decorate --all  # Compact log view
git diff                  # Show unstaged differences
git diff --staged         # Show staged differences

📌 8. Deleting & Untracking Files
git rm <file>             # Remove file from tracking & delete it
git rm --cached <file>    # Remove file from tracking but keep it

🔥 Bonus: One-Liner to Upload This File to GitHub
git add README.md && git commit -m "Added Git commands cheat sheet" && git push origin main
