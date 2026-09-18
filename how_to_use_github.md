How to configure and use GitHub

1. Go to project directory
```cd ~/path/to/directory```

Verify the files:
```ls```

2. Initialize the local Git repo (needs to be done only once per project)
```git init```

3. Create .gitignore
```nano .gitignore```

Example to add in the file:
# Python
__pycache__/
*.pyc

# Virtual environments
venv/
.venv/

# Credentials
.env
*.env
credentials.py
secrets.py

# SSH keys
*.pem
*.key

# macOS
.DS_Store

# VS Code
.vscode/

Never upload passwords, API tokens, SSH private keys, SNMP communities, enable secrets or other sensitive info.

4. Connect local repository to GitHub
Copy the HTTPS URL from GitHub → repository → Code → HTTPS.

Example:
```git remote add origin https://github.com/USERNAME/REPOSITORY.git```

Verify:
```git remote -v```

You should have 1 fetch file and 1 push file.

5. Check the files
```git status```

6. Stage the files
```git add .```

Check:
```git status```

7. Create the first commit
```git commit -m "Initial commit"```

If git doesn't know your identity, configure it:
```git config --global user.name "Your Name"```
```git config --global user.email "your-email@example.com"```

Then run the commit again.

8. Name the branch main
```git branch -M main```

9. Install GitHub CLI

On macOS with Homebrew:
```brew install gh```

On Ubuntu with apt:
```sudo apt install gh```

Verify:
```gh --version```

10. Authenticate with GitHub:
```gh auth login```

Select:
GitHub.com
HTTPS
Authenticate Git with your GitHub credentials? n
Login with a web browser

Complete authentication in your browser.

Verify:
```gh auth status```

11. Configure Git to use GitHub CLI authentication. (need to be done only once on the computer).
```gh auth setup-git```

12. Stage your files if you get an error
```git add.```

13.  And create again the first commit
```git commit -m "Initial commit"```

14. Make sure the branch is called main:
```git branch -M main```

Verify:
```git branch```
You should see: ```* main```

15. Push the project.
```git push -u origin main```

The -u estabilishes origin/main as the upstream branch. After that, you can normally just use:
```git push```

Once a repository is configured, you do not repeat all the steps above.

After creating or modifying scripts:
````bash
cd ~/path/to/project

git status
git diff
git add .
git status
git commit -m "Add interface status script"
git push

