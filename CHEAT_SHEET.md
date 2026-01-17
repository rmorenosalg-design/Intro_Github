# GitHub Quick Reference Cheat Sheet

A handy reference guide for common GitHub operations and commands.

## 🌐 GitHub Web Interface

### Creating a New Repository
1. Click the **+** icon in the top right corner
2. Select **New repository**
3. Fill in repository name and description
4. Choose public or private
5. Click **Create repository**

### Creating a Branch
1. Click the branch dropdown (shows "main" by default)
2. Type your new branch name
3. Click **Create branch**

### Making Changes Through Web Interface
1. Navigate to the file you want to edit
2. Click the pencil icon (✏️) to edit
3. Make your changes
4. Scroll down to the commit section
5. Add a commit message
6. Click **Commit changes**

### Opening a Pull Request
1. Click **Pull requests** tab
2. Click **New pull request**
3. Select the branch with your changes
4. Click **Create pull request**
5. Add a title and description
6. Click **Create pull request**

### Merging a Pull Request
1. Open the pull request
2. Review the changes
3. Click **Merge pull request**
4. Click **Confirm merge**
5. Optionally delete the branch

## 💻 Git Command Line Basics

### Setup and Configuration
```bash
# Set your name
git config --global user.name "Your Name"

# Set your email
git config --global user.email "your.email@example.com"

# Check your settings
git config --list
```

### Starting a Repository
```bash
# Initialize a new repository
git init

# Clone an existing repository
git clone https://github.com/username/repository.git
```

### Basic Workflow
```bash
# Check status of your files
git status

# Add files to staging area
git add filename.txt        # Add specific file
git add .                   # Add all changed files

# Commit your changes
git commit -m "Your commit message"

# Push changes to GitHub
git push origin main
```

### Branching
```bash
# Create a new branch
git branch branch-name

# Switch to a branch
git checkout branch-name

# Create and switch to new branch (shortcut)
git checkout -b branch-name

# List all branches
git branch

# Delete a branch
git branch -d branch-name
```

### Updating and Syncing
```bash
# Get latest changes from GitHub
git pull origin main

# Fetch changes without merging
git fetch origin

# Merge a branch into current branch
git merge branch-name
```

### Viewing History
```bash
# View commit history
git log

# View compact history
git log --oneline

# View changes in files
git diff

# View changes for a specific file
git diff filename.txt
```

## 🔑 Key Concepts

### The Git Workflow
1. **Modify** files in your working directory
2. **Stage** changes you want to commit (`git add`)
3. **Commit** staged changes (`git commit`)
4. **Push** commits to GitHub (`git push`)

### Branch Strategy
- **main/master**: The stable, production-ready code
- **feature branches**: Create these for new features or changes
- **Always branch**: Never work directly on main for new changes

### Commit Message Best Practices
- Use present tense ("Add feature" not "Added feature")
- Keep first line under 50 characters
- Be descriptive but concise
- Example: "Fix login button alignment on mobile"

## 📝 Common Terms

| Term | Description |
|------|-------------|
| **Repository** | A project folder tracked by Git |
| **Clone** | Download a copy of a repository |
| **Fork** | Create your own copy of someone else's repository |
| **Commit** | Save a snapshot of your changes |
| **Push** | Upload your commits to GitHub |
| **Pull** | Download and merge changes from GitHub |
| **Branch** | A separate line of development |
| **Merge** | Combine changes from different branches |
| **Pull Request** | Propose changes to be merged |
| **Remote** | A version of your repository hosted elsewhere (like GitHub) |
| **Origin** | The default name for your remote repository |

## 🆘 Common Issues and Solutions

### Problem: Changes not showing on GitHub
**Solution**: Make sure you've committed AND pushed your changes
```bash
git add .
git commit -m "Your message"
git push origin main
```

### Problem: Merge conflict
**Solution**: 
1. Open the conflicting files
2. Look for conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
3. Edit to keep the correct version
4. Remove the conflict markers
5. Commit the resolved files

### Problem: Want to undo last commit (not pushed yet)
**Solution**:
```bash
git reset HEAD~1  # Keeps changes but undoes commit
```

### Problem: Accidentally committed to wrong branch
**Solution**:
```bash
git stash              # Save your changes
git checkout correct-branch
git stash pop          # Apply your changes
```

## 🎯 Tips for Success

1. **Commit often**: Small, frequent commits are better than large ones
2. **Write good commit messages**: Your future self will thank you
3. **Pull before you push**: Always get the latest changes first
4. **Branch for features**: Keep your main branch clean
5. **Review before committing**: Use `git status` and `git diff`
6. **Use .gitignore**: Don't commit unnecessary files

## 📚 Learn More

- [GitHub Documentation](https://docs.github.com)
- [Pro Git Book](https://git-scm.com/book/en/v2) - Free and comprehensive
- [GitHub Learning Lab](https://lab.github.com)
- [Git Cheat Sheet (PDF)](https://education.github.com/git-cheat-sheet-education.pdf)

---

**Remember**: Practice makes perfect! The more you use Git and GitHub, the more natural it becomes. 🚀
