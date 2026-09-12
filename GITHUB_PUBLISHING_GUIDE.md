# GitHub Publishing Guide for Energy Game

This guide walks you through publishing your Energy Game project to GitHub step-by-step.

## Prerequisites

- GitHub account (free at [github.com](https://github.com))
- Git installed on your computer
- Your project files ready

## Step 1: Create a GitHub Account (if needed)

1. Visit [github.com](https://github.com)
2. Click "Sign up"
3. Enter email, password, username
4. Verify email
5. Complete setup

## Step 2: Create a New Repository on GitHub

1. **Log in to GitHub**
2. **Click the "+" icon** in the top right
3. **Select "New repository"**
4. **Fill in details:**
   - **Repository name:** `energy-game` (or your preferred name)
   - **Description:** "An interactive MATLAB educational game about clean vs unclean energy"
   - **Visibility:** Choose "Public" (everyone can see) or "Private" (only you and collaborators)
   - **Initialize with:** Leave unchecked for now
5. **Click "Create repository"**

You'll see a page with commands - **KEEP THIS PAGE OPEN**, you'll need it soon!

## Step 3: Prepare Your Local Project

On your computer, open a terminal/command prompt and navigate to your project folder:

```bash
cd path/to/your/energy-game
```

### If You Already Have Git Initialized

```bash
# Check if git is initialized
git status

# If it shows "fatal: not a git repository", do step below
```

### If Git is NOT Initialized Yet

```bash
# Initialize git
git init

# Configure git with your info (do this once)
git config --global user.name "Your Name"
git config --global user.email "your.email@gmail.com"

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Energy Game project"
```

## Step 4: Connect to GitHub Repository

In your terminal, run these commands (replace `yourusername` with your GitHub username):

```bash
# Add GitHub as remote repository
git remote add origin https://github.com/yourusername/energy-game.git

# Verify it's connected
git remote -v
# Should show:
# origin  https://github.com/yourusername/energy-game.git (fetch)
# origin  https://github.com/yourusername/energy-game.git (push)

# Rename default branch to main (modern best practice)
git branch -M main

# Push to GitHub
git push -u origin main
```

### If You See Authentication Error

GitHub now requires personal access tokens:

1. **On GitHub, go to:** Settings → Developer settings → Personal access tokens
2. **Click "Generate new token"**
3. **Configure token:**
   - Name: "energy-game-push"
   - Expiration: 30 days
   - Scopes: Check "repo"
4. **Click "Generate token"**
5. **Copy the token** (you won't see it again!)
6. **Use token as password:**
   ```bash
   git push -u origin main
   # Username: yourusername
   # Password: [paste token here]
   ```

Or use SSH keys (more secure but more complex):
[GitHub SSH Setup Guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

## Step 5: Verify on GitHub

1. **Go to your repository:** `github.com/yourusername/energy-game`
2. **You should see:**
   - All your files listed
   - README.md displayed nicely below the file list
   - File count matches your local project

## Step 6: Add Important Files (If Not Already Included)

Make sure these files are in your repository:

```bash
# Check what you have
ls -la

# Files should include:
# - README.md
# - LICENSE
# - .gitignore
# - CONTRIBUTING.md
# - Main MATLAB files
# - assets/ folder with images
```

If any are missing, add them:

```bash
# Add new files
git add [filename]
git commit -m "Add [filename]"
git push origin main
```

## Step 7: Create Additional GitHub Files (Optional but Recommended)

### Create CONTRIBUTORS.md

```bash
cat > CONTRIBUTORS.md << 'EOF'
# Contributors

## Project Team
- **Jonathan Yang** - Lead Developer, UI/UX, Graphics
- **Alex** - Game Logic, Mechanics

## How to Contribute
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.
EOF

git add CONTRIBUTORS.md
git commit -m "Add contributors list"
git push origin main
```

### Create a Changelog

```bash
cat > CHANGELOG.md << 'EOF'
# Changelog

All notable changes to this project will be documented in this file.

## [1.0.0] - 2026-09-12

### Added
- Initial public release
- Core game mechanics
- 3 educational question sets
- Menu and game-over screens
- Score tracking with CO₂ and renewable metrics
- Retro pixel art graphics

### Contributors
- Jonathan Yang
- Alex
EOF

git add CHANGELOG.md
git commit -m "Add changelog"
git push origin main
```

## Step 8: Set Up GitHub Features

### Add Topics (Tags)

On your repository page:
1. Click the gear icon ⚙️ (Settings)
2. Find "Topics" section
3. Add: `matlab`, `education`, `game`, `energy`, `environment`
4. Click save

### Add a Description and Website

1. Go to repository main page
2. Click pencil icon next to description
3. Add: "Interactive MATLAB game teaching about clean vs unclean energy"
4. Optionally add a website link
5. Save

### Enable GitHub Pages (for documentation)

1. Go to Settings → Pages
2. Select "main" branch
3. Select "/root" folder
4. Save
5. Your site will be available at: `https://yourusername.github.io/energy-game`

## Step 9: Create a Release

To let people download specific versions:

1. Go to your repository
2. Click "Releases" on the right sidebar
3. Click "Create a new release"
4. **Tag version:** `v1.0.0`
5. **Title:** "Energy Game v1.0.0"
6. **Description:** Include what's new
7. Click "Publish release"

## Step 10: Create Issues for Future Work

Help guide contributions:

1. Go to "Issues" tab
2. Click "New issue"
3. Create issues for:
   - Bugs you know about
   - Features you want to add
   - Documentation improvements
   - Questions from future contributors

**Example:**
```
Title: Add difficulty levels
Body: Create Easy/Medium/Hard modes with different numbers of questions
Labels: enhancement, feature-request
```

## Making Updates Later

When you make changes and want to push to GitHub:

```bash
# Make your changes, then:
git add .                                    # Stage changes
git commit -m "Clear message about changes"  # Commit
git push origin main                         # Push to GitHub
```

## Useful GitHub Features

### 1. **Badges in README**

Add to your README to show project status:

```markdown
![GitHub License](https://img.shields.io/github/license/yourusername/energy-game)
![GitHub Release](https://img.shields.io/github/v/release/yourusername/energy-game)
![GitHub Issues](https://img.shields.io/github/issues/yourusername/energy-game)
```

### 2. **Branch Protection**

To require reviews before merging to main:

1. Settings → Branches
2. "Add rule"
3. Pattern: `main`
4. Check "Require pull request reviews"

### 3. **GitHub Issues Templates**

Create `.github/ISSUE_TEMPLATE/bug_report.md`:

```markdown
---
name: Bug report
about: Create a report to help us improve

---

**Describe the bug**
A clear description of the problem.

**To Reproduce**
Steps to reproduce the behavior:
1. ...

**Expected behavior**
What should happen.

**Environment:**
- MATLAB version: 
- OS: 
```

## Tips for a Great GitHub Project

1. ✅ **Write a detailed README** - Best first impression
2. ✅ **Include a LICENSE** - Protects your work
3. ✅ **Create CONTRIBUTING.md** - Encourages contributions
4. ✅ **Respond to issues** - Show you're active
5. ✅ **Update regularly** - Keep project alive
6. ✅ **Add examples** - Show what the project does
7. ✅ **Use issues** - Organize future work
8. ✅ **Add badges** - Visual project status
9. ✅ **Document thoroughly** - Help developers understand
10. ✅ **Be welcoming** - Encourage community

## Troubleshooting

### "fatal: origin already exists"
```bash
git remote remove origin
git remote add origin https://github.com/yourusername/energy-game.git
```

### "The current branch main has no upstream branch"
```bash
git push -u origin main
```

### "Everything up-to-date" but nothing appeared on GitHub
- Check if you committed: `git log` should show commits
- Verify remote: `git remote -v`
- Try: `git push -f origin main` (⚠️ use carefully)

### Can't find my repository
- Check you're logged in to correct GitHub account
- URL should be: `github.com/your-username/energy-game`
- Clear browser cache if needed

### Authentication failed
Use personal access token instead of password:
1. GitHub Settings → Personal access tokens
2. Generate new token (check "repo")
3. Use token as password when pushing

## Next Steps

1. **Promote your project:**
   - Share on social media
   - Post on Reddit/Discord communities
   - Add to MATLAB Central
   - Include in education blogs

2. **Engage with community:**
   - Respond to issues promptly
   - Merge pull requests
   - Thank contributors
   - Keep documentation updated

3. **Continue development:**
   - Add new questions
   - Improve graphics
   - Add new features
   - Fix reported bugs

## Additional Resources

- [GitHub Docs](https://docs.github.com)
- [Git Tutorial](https://git-scm.com/doc)
- [Markdown Guide](https://www.markdownguide.org)
- [GitHub Community](https://github.community)

---

**Congratulations! Your Energy Game is now on GitHub! 🎉**

Questions? Check GitHub's help documentation or ask in GitHub Discussions.
