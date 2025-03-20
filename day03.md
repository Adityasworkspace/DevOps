# Git Setup and Push to GitHub

### Follow these steps to install Git, create a file, and push it to your GitHub repository.

---

## Step 1: Install Git

If Git is not already installed on your system, use the following commands:

```bash
sudo yum install git -y
git --version
```

## Step 2: Set Up Your Git Working Directory
Navigate to your desired directory:

```bash
cd ..
```

Switch to root user if needed:

```bash
sudo -i
```

Create a new directory for your project:

```bash
mkdir gitfile
```

Navigate into the project directory:

```bash
cd gitfile
```

Create a new file in the directory:

```bash
touch optimus.html
```

## Step 3: Initialize Git Repository

Initialize a new Git repository:

```bash
git init
```

Check the Status of the Repository (to see untracked files):

```bash
git status
```

Add the File to the Staging Area:
```bash
git add optimus.html
```

Alternatively, Add All Files (If you want to add all files, use git add . instead):
```bash
git add .
```

Check the Status Again (to verify that the file is staged):
```bash
git status
```

Commit the changes with a message:
```bash
git commit -m "initial commit"
```

View the commit log:

```bash
git log
```

## Step 5: Configure Git User Details

Set your GitHub username (replace opoptimus with your actual GitHub username):

```bash
git config --global user.name "opoptimus"
```

Set your GitHub email (replace with your GitHub email):

```bash
git config --global user.email "your-email@example.com"
```
Verify the Git configuration:

```bash
git config --global --list
```
## Step 6: Add Remote Repository

Add the GitHub remote repository (replace with your actual repository URL):

```bash
git remote add origin https://github.com/opOPTIMUS/DEVOPS.git
```
Push your changes to the remote repository:

```bash
git push -u origin master
```
## Step 7: Create a GitHub Personal Access Token (PAT)

1 Go to GitHub and log in to your account.

2 Click on your profile icon in the top-right corner and go to Settings.

3 Scroll down and click on Developer settings.

4 In the left sidebar, select Personal access tokens under Developer settings.

5 Click Generate new token.

6 Provide a note (e.g., Git operations on my repo) and select repo scope.

7 Click Generate token and copy the token (you won’t be able to see it again).

## Step 8: Use the Personal Access Token (PAT)

1 After running git push, you’ll be prompted for your GitHub username and password.

2 Use your GitHub username as usual.

3 Paste the PAT as the password instead of your GitHub password.

Example:

```rust
Username for 'https://github.com': opoptimus
Password for 'https://opoptimus@github.com': <paste your PAT here>
```

## Step 9: Verify the Push on GitHub

1 After pushing, go to your repository on GitHub (https://github.com/opOPTIMUS/######).

2 Verify that the optimus.html file has been successfully pushed.

3 You may also see a link to create a pull request if needed.


# Final Recap of Commands:
```bash
# Step 1: Install Git
sudo yum install git -y
git --version

# Step 2: Set Up Your Project Directory
mkdir gitfile
cd gitfile

# Step 3: Initialize Git Repository
git init
git status

# Step 4: Add and Commit the File
touch optimus.html
git add optimus.html
git commit -m "initial commit"
git log

# Step 5: Configure User Info
git config --global user.name "opoptimus"
git config --global user.email "your-email@example.com"
git config --global --list

# Step 6: Add Remote Repo and Push
git remote add origin https://github.com/opOPTIMUS/DEVOPS.git
git push -u origin master
```
=============================X=============================X================================

# To determine whether to push to the main or master branch on GitHub, follow these steps:

### Check the Default Branch on GitHub:
On your repository's GitHub page, the default branch (either main or master) is displayed in the branch dropdown. If your repository is newly created, it likely uses main as the default. If it’s an older repository, it might still use master.

### Check Your Local Branch:
Use the command git branch to see which branch you’re currently working on. The active branch will be highlighted with an asterisk (*). If you're on main, you’ll push to main. If you’re on master, you’ll push to master.

### Push to the Correct Branch:
If the default branch is main, push to main with:

```bash
git push -u origin main
```

If the default branch is master, push to master with:
```bash
git push -u origin master
```

### Changing the Default Branch (if needed):

You can change the default branch in the GitHub repository settings under the Branches section. Select either main or master and update accordingly.

By following these steps, you can ensure that you’re pushing to the correct branch on GitHub.
