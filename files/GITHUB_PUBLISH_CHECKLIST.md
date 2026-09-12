# GitHub Publication Checklist

Complete this checklist before publishing your project to GitHub.

## Pre-Publication Setup

### Repository Creation
- [ ] Create new repository on GitHub
- [ ] Name: `Energy-Game-Clean-vs-Unclean`
- [ ] Description: "Interactive educational puzzle-quiz game about energy sources built with MATLAB"
- [ ] Make repository public
- [ ] Add topics: `matlab`, `educational-game`, `pixel-art`, `energy`, `science`
- [ ] Choose LICENSE: MIT License

### Git Configuration (First Time Only)
```bash
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## File Checklist

All essential files are created and ready:

### Root Files
- [x] **README.md** - Main project documentation
- [x] **LICENSE** - MIT License
- [x] **.gitignore** - Ignore MATLAB and OS-specific files
- [x] **CONTRIBUTING.md** - Contribution guidelines
- [x] **QUICK_START.md** - 5-minute getting started guide

### Documentation Folder (`docs/`)
- [x] **DESIGN.md** - Complete game design documentation
- [x] **SETUP_GUIDE.md** - Detailed installation and troubleshooting

### GitHub Configuration (`.github/`)
- [x] **ISSUE_TEMPLATE/bug_report.md** - Bug report template
- [x] **ISSUE_TEMPLATE/feature_request.md** - Feature request template

### Project Files (Verify Locally)
- [ ] All source code files in `src/` folder:
  - `Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m`
  - `simpleGameEngine.m`
  - `SDP_MenuEnd_AND_GameScene.m`
  - `SDP_Menu_Page.m`
  
- [ ] All sprite assets in `assets/sprites/`:
  - `Menu.png`
  - `Question_1_Page.png`
  - `Question_2_page.png`
  - `Question_3_page.png`
  - `Endgame_Background.png`
  - Any other sprite sheets

- [ ] Documentation PDFs in `docs/`:
  - `SDP_Notebook_Group_L_AU_25.pdf` (project notes)
  - `SDP_Game.pdf` (game design)

- [ ] Example files (optional but recommended):
  - `example_script.m`
  - `SDP_Preview.m`

## Content Quality Checks

### README.md
- [ ] Project title and description are clear
- [ ] Table of contents or navigation present
- [ ] Installation instructions are complete
- [ ] Usage/gameplay instructions are clear
- [ ] Contact information or support links included
- [ ] License information referenced
- [ ] All links are functional

### CONTRIBUTING.md
- [ ] Code style guidelines provided
- [ ] Commit message format explained
- [ ] PR process documented
- [ ] Issue templates described
- [ ] Types of contributions wanted listed

### Documentation
- [ ] All markdown files have clear headings
- [ ] Code examples are properly formatted
- [ ] No broken links or references
- [ ] Spelling and grammar checked
- [ ] Technical accuracy verified

## Git Setup

### Initialize Git Repository
```bash
cd /path/to/Energy-Game-Clean-vs-Unclean

# Initialize git
git init

# Add all files
git add .

# Create initial commit
git commit -m "Initial commit: Add Energy Game project files"

# Rename branch to main (if needed)
git branch -M main
```

### Add Remote and Push
```bash
# Add remote repository
git remote add origin https://github.com/yourusername/Energy-Game-Clean-vs-Unclean.git

# Push to GitHub
git push -u origin main
```

## GitHub Repository Configuration

### Settings
- [ ] Go to repository **Settings**
- [ ] Set repository visibility to **Public**
- [ ] Enable **Issues** (for bug reports and features)
- [ ] Enable **Discussions** (for community feedback)
- [ ] Enable **Projects** (for tracking development)
- [ ] Disable **Wikis** (using docs instead)
- [ ] Set default branch to **main**

### Branch Protection
- [ ] Go to **Settings** → **Branches**
- [ ] Click **Add rule** for `main` branch
- [ ] Require pull request reviews before merging (2+ reviews recommended)
- [ ] Require status checks to pass before merging (once CI/CD setup)
- [ ] Require branches to be up to date before merging

### Topics/Tags
- [ ] Add repository topics (click gear icon):
  - `matlab`
  - `educational-game`
  - `puzzle-game`
  - `energy`
  - `environmental-science`
  - `pixel-art`

### README Preview
- [ ] Visit your repository
- [ ] Verify README displays correctly
- [ ] Check all links work
- [ ] Confirm images display properly

## Documentation Completeness Check

### User-Facing Documentation
- [x] How to install
- [x] How to run
- [x] How to play
- [x] Controls reference
- [x] Troubleshooting guide
- [x] FAQ

### Developer Documentation
- [x] Architecture overview
- [x] Code organization
- [x] Component descriptions
- [x] Contributing guidelines
- [x] Issue templates
- [x] Code style guide

### Project Information
- [x] Game design document
- [x] Learning objectives
- [x] Gameplay mechanics
- [x] Project roadmap (future ideas)
- [x] License information
- [x] Creator attribution

## Social/Sharing Setup

### GitHub Profile
- [ ] Update profile with repository link
- [ ] Add "Energy Game" to profile bio or featured projects
- [ ] Create project release (v1.0.0):
  ```bash
  git tag v1.0.0
  git push origin v1.0.0
  ```

### Publish Release on GitHub
- [ ] Go to **Releases**
- [ ] Click **Create a new release**
- [ ] Version: `v1.0.0`
- [ ] Title: `Energy Game v1.0.0 - Initial Release`
- [ ] Description:
  ```
  First official release of Energy Game: Clean vs Unclean
  
  ## Features
  - Three educational chapters (Coal, Petroleum, Wind Energy)
  - Interactive quiz questions
  - Puzzle-based cleaning mechanics
  - Pixel art visual style
  
  ## Requirements
  - MATLAB R2016b+
  - Image Processing Toolbox
  
  See README.md for installation and gameplay instructions.
  ```
- [ ] Publish release

### Social Media Sharing (Optional)
- [ ] Share on Twitter/X: "Just published my MATLAB educational game! #GameDev #Education"
- [ ] Share on LinkedIn: Project description and GitHub link
- [ ] Share on Reddit: r/GameDev, r/MATLAB, r/EnvironmentalScience (if appropriate)

## Final Quality Checks

### Code Quality
- [ ] Run all code locally one more time
- [ ] Verify all features work as documented
- [ ] No console errors or warnings
- [ ] Game completes all 3 chapters successfully
- [ ] Both quiz and puzzle mechanics function correctly

### File Integrity
- [ ] No large binary files accidentally committed
- [ ] Sprite images display correctly
- [ ] PDF documents intact and readable
- [ ] No personal information in code or commits

### Documentation Accuracy
- [ ] All file paths in documentation match actual structure
- [ ] Code examples execute without modification
- [ ] Installation instructions produce working game
- [ ] All referenced files exist and are accessible
- [ ] No broken links or incorrect GitHub URLs

## Post-Publication

### Immediate Actions
- [ ] Verify repository is accessible publicly
- [ ] Test clone from command line works
- [ ] Verify installation instructions work
- [ ] Confirm README displays perfectly
- [ ] Test all issue templates work

### Announcement
- [ ] Share GitHub link with instructors/classmates
- [ ] Post to school forum/discussion board
- [ ] Send to collaborators/team members
- [ ] Add to your portfolio/resume

### Ongoing Maintenance
- [ ] Monitor issues for bug reports
- [ ] Respond to pull requests
- [ ] Keep documentation up to date
- [ ] Create milestone tags for version releases
- [ ] Celebrate your completed project! 🎉

## Troubleshooting During Publication

### Problem: Large files prevent push
**Solution:** Ensure `.gitignore` is working:
```bash
git check-ignore -v *   # See what's ignored
git clean -fd           # Remove untracked files
```

### Problem: README has formatting issues
**Solution:** 
- Use [GitHub Markdown Preview](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
- Validate with [Markdown Lint](https://www.markdownlint.com/)

### Problem: Images don't display in GitHub
**Solution:**
- Use relative paths: `![Alt](assets/sprites/Menu.png)`
- Not absolute paths: `![Alt](/home/claude/assets/sprites/Menu.png)`
- Verify images are committed: `git ls-files | grep .png`

### Problem: Repository not showing in search
**Solution:**
- GitHub search takes time to index (up to 24 hours)
- Add meaningful description and topics
- Create first release to boost visibility

## Sign-Off

- [ ] All checks completed
- [ ] Code tested and verified
- [ ] Documentation reviewed
- [ ] Repository configured
- [ ] Ready to publish!

---

## Next Steps After Publishing

1. **Get Feedback**: Open GitHub Discussions for community feedback
2. **Track Issues**: Use GitHub Issues to track bugs and features
3. **Grow Contributors**: Promote CONTRIBUTING.md to attract collaborators
4. **Iterate**: Use GitHub Projects to manage development roadmap
5. **Keep Updated**: Update README and docs as the project evolves

---

**Publication Date**: [Your Date]
**Repository URL**: https://github.com/[username]/Energy-Game-Clean-vs-Unclean
**Status**: ✓ Ready to Publish
