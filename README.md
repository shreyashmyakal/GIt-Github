# Git & GitHub for Beginners: A Complete Guide
📌 What is Git?
Git is a distributed version control system (DVCS) that helps developers track changes in their source code during software development.

VCS (Version Control System): Tracks changes in your files over time.

SCM (Source Code Management): Manages source code with features like branching, merging, and history tracking.

Project Tracking System: Helps track versions, contributions, and collaborations among team members.

📦 Git Repository
A repository (repo) is a project folder that Git tracks. It includes:

The source code

All change history

Metadata, branches, and tags

Repositories can be:

Local: On your system

Remote: On platforms like GitHub, GitLab, Bitbucket

🛠 How to Install Git
Windows / macOS / Linux:
Download from https://git-scm.com/

Install with default settings

Verify installation by running:

bash
Copy
Edit
git --version
📁 What is git init?
git init initializes a new Git repository in your current folder.
It creates a Git workspace with 3 main stages:

pgsql
Copy
Edit
Working Directory (Untracked files)
       |
       | git add
       ▼
Staging Area (Ready to be committed)
       |
       | git commit
       ▼
Git Repository (Committed files)
Command to initialize:

bash
Copy
Edit
git init
🛠 Git Configuration
Set your identity for commits:

bash
Copy
Edit
git config --global user.name "Shreyash Myakal"
git config --global user.email "shreyashmyakal@gmail.com"
Check your configuration:

bash
Copy
Edit
git config --list
🧷 Linking Git to GitHub
Create a repository on GitHub.

Link your local folder to GitHub remote repo:

bash
Copy
Edit
git remote add origin https://github.com/username/repo-name.git
Pull existing remote repository branch:

bash
Copy
Edit
git pull origin main
🔨 Common Git Commands
Add all files to staging:

bash
Copy
Edit
git add .
Commit staged files with a message:

bash
Copy
Edit
git commit -m "Initial commit"
Push commits to GitHub (main branch):

bash
Copy
Edit
git push origin main
🔐 What is a GitHub Token?
When Two-Factor Authentication (2FA) is enabled, GitHub requires Personal Access Tokens instead of passwords during git push.

How to Create a GitHub Token:
Go to GitHub > Settings > Developer Settings > Tokens (Classic)

Click Generate New Token

Select scopes (e.g., repo, workflow)

Copy and use this token as your password during git push

🧪 Git Status Variants
Full status:

bash
Copy
Edit
git status
Short status:

bash
Copy
Edit
git status -s
Status symbols:

?? = Untracked files

M = Modified

A = Added

🔍 Git Diff Variants
Show unstaged changes:

bash
Copy
Edit
git diff
Show staged but uncommitted changes:

bash
Copy
Edit
git diff --staged
Compare working directory with last commit:

bash
Copy
Edit
git diff HEAD
📝 View Commits
Show full commit history:

bash
Copy
Edit
git log
Show details of latest commit:

bash
Copy
Edit
git show
Show specific commit by hash:

bash
Copy
Edit
git show <hash>
🙈 Git Ignore
Use a .gitignore file to exclude files/folders from being tracked by Git.

🔁 Git Reset Explained with git status
Add files to staging area:

bash
Copy
Edit
git add .
git status
Unstage a file (move from staging back to working directory):

bash
Copy
Edit
git reset HEAD filename
git status
Undo last commit but keep changes staged:

bash
Copy
Edit
git reset --soft HEAD~1
git status
Undo last commit and unstage changes (keep changes in working directory):

bash
Copy
Edit
git reset --mixed HEAD~1
git status
Undo last commit and discard changes completely:

bash
Copy
Edit
git reset --hard HEAD~1
🧩 Git Workspace Diagram (Simplified)
sql
Copy
Edit
Working Directory
     │
 git add
     ▼
 Staging Area
     │
 git commit
     ▼
 Local Repository
     │
 git push
     ▼
 Remote Repository (GitHub)
✅ Final Summary
Command	Description
git init	Initialize a new repo
git add .	Add all changes to staging
git commit -m "msg"	Save changes with message
git status / git status -s	View changes (full / short)
git diff / git diff --staged	View differences (unstaged / staged)
git push origin main	Upload code to GitHub main branch
git log / git show	See commit history and details
git reset --soft HEAD~1	Undo commit but keep staged
git reset --mixed HEAD~1	Undo commit and unstage changes
git reset --hard HEAD~1	Undo commit and delete changes


