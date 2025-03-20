# Git

## Table of Contents

- [Introduction](#introduction)
- [Git Basics](#git-basics)
  - [What is Git?](#what-is-git)
  - [Installation](#installation)
  - [Essential Git Commands](#essential-git-commands)
  - [Git Workflow Diagram](#git-workflow-diagram)
  - [Typical Git Workflow](#typical-git-workflow)
- [GitHub](#github)
  - [What is GitHub?](#what-is-github)
  - [Key GitHub Concepts](#key-github-concepts)
  - [Setting Up a GitHub Repository](#setting-up-a-github-repository)
  - [Working with Branches](#working-with-branches)
- [Git Bash](#git-bash)
  - [Common Bash Commands](#common-bash-commands)
  - [Useful Shortcuts](#useful-shortcuts)
- [GitHub CLI (`gh`)](#github-cli-gh)
  - [Installation](#installation-1)
  - [Common GitHub CLI Commands](#common-github-cli-commands)
- [Workflow: Creating a Repo and Uploading Local Files from Git Bash Using GitHub CLI](#workflow-creating-a-repo-and-uploading-local-files-from-git-bash-using-github-cli)
  - [Step-by-Step Guide](#step-by-step-guide)
- [7. Best Practices for Data Analysts](#7-best-practices-for-data-analysts)


## **Introduction**

Git and GitHub are essential tools for version control, collaboration, and tracking changes in code. As a data analyst, you’ll use them to manage scripts, notebooks, and datasets efficiently.

## **Git Basics**

### **What is Git?**

Git is a distributed version control system that tracks file changes and enables collaboration.

### **Installation**

- Download Git from [Git’s official site](https://git-scm.com/downloads).
- Verify installation:
    
    ```bash
    git --version
    ```
    

### **Essential Git Commands**

| Command | Description |
| --- | --- |
| `git init` | Initialize a new Git repository |
| `git clone <repo_url>` | Clone an existing repository |
| `git status` | Check working directory status |
| `git add <file>` | Stage file(s) for commit |
| `git commit -m "message"` | Save changes to Git history |
| `git log` | View commit history |
| `git branch` | List branches |
| `git checkout <branch>` | Switch branches |
| `git merge <branch>` | Merge branches |
| `git pull` | Update local repo from remote |
| `git push` | Upload changes to GitHub |

### Git Workflow Diagram

### **Typical Git Workflow**

1. **Initialize a repository**
    
    ```bash
    git init
    ```
    
2. **Clone an existing repository**
    
    ```bash
    git clone <repo_url>
    ```
    
3. **Make changes and commit**
    
    ```bash
    git add .
    git commit -m "Your commit message"
    ```
    
4. **Push changes to GitHub**
    
    ```bash
    git push origin main
    ```
    

## **GitHub**

### **What is GitHub?**

GitHub is a cloud-based platform for hosting Git repositories, enabling collaboration.

### **Key GitHub Concepts**

- **Repository (Repo)**: Stores project files and history.
- **Branch**: A version of a project to develop features separately.
- **Pull Request (PR)**: Proposed changes that need approval before merging.
- **Fork**: A personal copy of another user’s repo.
- **Issues**: Used for bug tracking and task management.
- **Actions**: Automate workflows like CI/CD.

### **Setting Up a GitHub Repository**

1. Create a new repository on GitHub.
2. Copy the repo URL.
3. Link the local project to GitHub:
    
    ```bash
    git remote add origin <repo_url>
    git push -u origin main
    ```
    

### **Working with Branches**

- Create a new branch:
    
    ```bash
    git checkout -b new-branch
    ```
    
- Push the branch to GitHub:
    
    ```bash
    git push -u origin new-branch
    ```
    
- Open a pull request on GitHub.

## **Git Bash**

Git Bash is a command-line tool for Git on Windows.

### **Common Bash Commands**

| Command | Description |
| --- | --- |
| `ls` | List files |
| `cd <directory>` | Change directory |
| `pwd` | Print working directory |
| `mkdir <name>` | Create a new directory |
| `rm <file>` | Delete a file |
| `clear` | Clear the terminal |

### **Useful Shortcuts**

- `Tab`: Auto-complete commands.
- `Ctrl + L`: Clear the terminal.

## **GitHub CLI (`gh`)**

GitHub CLI lets you manage GitHub from the terminal.

### **Installation**

- Download from [GitHub CLI](https://cli.github.com/).
- Authenticate:
    
    ```bash
    gh auth login
    ```
    

### **Common GitHub CLI Commands**

| Command | Description |
| --- | --- |
| `gh repo clone <repo>` | Clone a GitHub repository |
| `gh repo create <name>` | Create a GitHub repository |
| `gh issue list` | List repo issues |
| `gh pr create` | Create a pull request |
| `gh pr merge` | Merge a pull request |

## **Workflow: Creating a Repo and Uploading Local Files from Git Bash Using GitHub CLI**

Instead of creating a repository via the GitHub website, you can do it directly from the command line.

### **Step-by-Step Guide**

1. **Navigate to your project directory**
    
    Open Git Bash and move to the directory where your project files are stored:
    
    ```bash
    cd /path/to/your/project
    ```
    
2. **Initialize a new Git repository**
    
    This sets up Git in your local project folder:
    
    ```bash
    git init
    ```
    
3. **Check the status of your files**
    
    View which files are untracked or modified:
    
    ```bash
    git status
    ```
    
4. **Stage all files for commit**
    
    This adds all files in the directory to Git:
    
    ```bash
    git add .
    ```
    
5. **Confirm staged files**
    
    Verify that files have been added:
    
    ```bash
    git status
    ```
    
6. **Commit your changes**
    
    Save the staged files with a descriptive message:
    
    ```bash
    git commit -m "Initial commit"
    ```
    
7. **Create a new GitHub repository using GitHub CLI**
    
    Instead of manually creating a repository on GitHub, use:
    
    ```bash
    gh repo create <repo_name> --public --source=. --remote=origin
    ```
    
    This creates a **public repository**, sets it as the remote, and links it to your local project.
    
8. **Verify the remote repository**
    
    Ensure that the link to GitHub was added correctly:
    
    ```bash
    git remote -v
    ```
    
9. **Push your local project to GitHub**
    
    Upload the files from your local system to GitHub:
    
    ```bash
    git push -u origin main
    ```
    

Now, your project is successfully uploaded to GitHub, and any future changes can be committed and pushed using `git commit` and `git push`.

## **7. Best Practices for Data Analysts**

1. **Write clear commit messages** (e.g., `git commit -m "Added data cleaning script"`).
2. **Organize your repository** (`/data`, `/scripts`, `/notebooks`).
3. **Use branches for different features** to keep `main` clean.
4. **Pull updates regularly** (`git pull`) to stay up to date.
5. **Use `.gitignore`** to exclude unnecessary files (e.g., datasets, temp files).
6. **Maintain a `README.md`** to explain the project and instructions.
