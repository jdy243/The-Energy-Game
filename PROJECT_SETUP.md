# Energy Game - Project Setup Checklist

Use this checklist to prepare your project for GitHub publication and ensure everything is ready.

## Pre-Publication Checklist

### Project Files
- [x] Main game file (`Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m`)
- [x] Game engine (`simpleGameEngine.m`)
- [x] Menu system (`SDP_Menu_Page.m`)
- [x] Game scenes (`SDP_MenuEnd_AND_GameScene.m`)
- [x] Preview/setup (`SDP_Preview.m`)
- [x] Utilities (`Mathslime.m`)
- [x] Sprite assets (`retro_pack.png`, `Menu.png`)
- [ ] Documentation (`SDP_Game.pdf`, `SDP_Jonathan_AI_Useage.pdf`, `SDP_Notebook_Group_L_AU_25__1_.pdf`)

### Documentation Files
- [x] README.md ✅ Created
- [x] LICENSE ✅ Created (MIT)
- [x] CONTRIBUTING.md ✅ Created
- [x] .gitignore ✅ Created
- [x] CHANGELOG.md ✅ Ready to create
- [x] CONTRIBUTORS.md ✅ Ready to create
- [ ] CODE_OF_CONDUCT.md (Optional, recommended for community projects)

### Code Quality
- [ ] Remove debugging code and console outputs
- [ ] Check for hardcoded paths (should use relative paths)
- [ ] Verify all external dependencies are documented
- [ ] Ensure comments explain complex logic
- [ ] Test game runs without errors
- [ ] Test on MATLAB R2023b or later
- [ ] Verify all sprite assets are included

### GitHub Setup
- [ ] Create GitHub account (free)
- [ ] Create new repository named "energy-game"
- [ ] Set repository visibility (Public recommended)
- [ ] Initialize git locally
- [ ] Configure git user name and email
- [ ] Add files to git: `git add .`
- [ ] Create initial commit
- [ ] Add GitHub remote: `git remote add origin ...`
- [ ] Push to GitHub: `git push -u origin main`

### GitHub Repository Configuration
- [ ] Add repository description
- [ ] Add repository topics (tags): matlab, education, game, energy, environment
- [ ] Add repository website (if applicable)
- [ ] Verify README displays correctly
- [ ] Check all files are visible
- [ ] Create first release/tag

### Optional GitHub Features
- [ ] Create GitHub Pages for documentation
- [ ] Set up branch protection for main
- [ ] Add issue templates
- [ ] Add pull request template
- [ ] Enable discussions
- [ ] Create issue labels (bug, enhancement, documentation, etc.)

## Directory Structure

Your repository should look like this:

```
energy-game/
│
├── README.md                    ← Main documentation
├── LICENSE                      ← MIT License
├── CONTRIBUTING.md              ← Contribution guidelines
├── CHANGELOG.md                 ← Version history
├── CONTRIBUTORS.md              ← List of contributors
├── .gitignore                   ← Git ignore rules
├── GITHUB_PUBLISHING_GUIDE.md   ← This guide
├── PROJECT_SETUP.md             ← Setup checklist
│
├── assets/                      ← Image and sprite assets
│   ├── Menu.png
│   ├── retro_pack.png
│   ├── Menu_Background.png
│   ├── Question_1_Page.png
│   ├── Question_2_page.png
│   ├── Question_3_page.png
│   ├── Endgame_Background.png
│   └── [other images]
│
├── src/                         ← Source code (optional organization)
│   ├── Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m
│   ├── simpleGameEngine.m
│   ├── SDP_Menu_Page.m
│   ├── SDP_MenuEnd_AND_GameScene.m
│   ├── SDP_Preview.m
│   └── Mathslime.m
│
├── docs/                        ← Documentation
│   ├── SDP_Game.pdf
│   ├── SDP_Jonathan_AI_Useage.pdf
│   └── SDP_Notebook_Group_L_AU_25__1_.pdf
│
├── examples/                    ← Example usage (optional)
│   └── [example files]
│
└── .github/                     ← GitHub-specific files (optional)
    ├── ISSUE_TEMPLATE/
    │   └── bug_report.md
    ├── PULL_REQUEST_TEMPLATE.md
    └── workflows/               ← CI/CD workflows (optional)
        └── matlab-tests.yml
```

## Code Quality Standards

### Before Publishing, Ensure:

1. **No Debug Code**
   - Remove `disp()` statements for debugging
   - Remove `keyboard` or `pause` debugging commands
   - Clean console output

2. **Proper Comments**
   - All functions have headers explaining purpose
   - Complex logic has inline comments
   - Comments use complete sentences
   - Example:
     ```matlab
     % Correct: Clear, explains why
     % Pause game when player loses focus
     pause_game = true;
     
     % Avoid: Obvious comments
     % i = i + 1;  % increment i
     ```

3. **Variable Naming**
   - Use descriptive names: `playerScore` not `ps`
   - Use camelCase: `questionNumber` not `question_number`
   - Use UPPERCASE for constants: `MAX_PLAYERS = 10`

4. **Path Handling**
   - Use relative paths: `load('assets/menu.png')`
   - Avoid absolute paths: `load('C:/Users/John/energy-game/menu.png')`
   - Document required file structure

5. **Error Handling**
   - Add try-catch for file operations
   - Provide helpful error messages
   - Example:
     ```matlab
     try
         img = imread('assets/Menu.png');
     catch ME
         error('Failed to load Menu.png: %s', ME.message);
     end
     ```

## Testing Before Publication

### Manual Testing Checklist

- [ ] Game starts without errors
- [ ] Menu displays correctly
- [ ] Can start a new game
- [ ] Question 1 displays properly
  - [ ] All 4 answers are clickable
  - [ ] Answer selection works
  - [ ] Moves to next question
- [ ] Question 2 displays properly
  - [ ] All 4 answers are clickable
  - [ ] Answer selection works
  - [ ] Moves to game over screen
- [ ] Question 3 displays properly (if it exists)
- [ ] Game over screen shows results
  - [ ] Shows CO₂ reduction percentage
  - [ ] Shows renewable energy share
  - [ ] Replay button works
  - [ ] Exit button works
- [ ] Graphics display correctly
  - [ ] All sprites render properly
  - [ ] No missing images
  - [ ] Colors are correct
- [ ] Audio (if any) works
- [ ] Game is playable start to finish without crashes

### MATLAB Version Testing

- [ ] Tested on MATLAB R2023b
- [ ] Tested on MATLAB R2024a
- [ ] Tested on MATLAB R2024b
- [ ] Note any version-specific issues

### Operating System Testing

- [ ] Tested on Windows
- [ ] Tested on macOS (if possible)
- [ ] Tested on Linux (if possible)
- [ ] Document OS-specific requirements

## Documentation Checklist

### README.md Should Include

- [x] Project title and description
- [x] Project overview/purpose
- [x] Key features
- [x] Installation instructions
- [x] Usage instructions
- [x] Project structure
- [x] Requirements/dependencies
- [x] Contributors
- [x] License information
- [x] How to contribute
- [x] Contact/support information

### README.md Quality Check

- [ ] No broken links
- [ ] Code examples run without errors
- [ ] Screenshots display correctly
- [ ] Markdown formatting is clean
- [ ] No spelling errors
- [ ] Instructions are clear and complete
- [ ] All file paths are correct

## Content Preparation

### For GitHub Repository Page

1. **Prepare Description** (160 characters max)
   ```
   Interactive MATLAB educational game about clean vs unclean energy
   ```

2. **Select Topics** (up to 30)
   - matlab
   - education
   - game-development
   - energy
   - environmental-science
   - sustainability
   - stem-education

3. **Write About Section**
   ```
   Energy Game is an interactive MATLAB-based game designed to teach 
   students about clean and unclean energy sources, their environmental 
   impacts, and the importance of sustainable energy choices.
   ```

### Repository Screenshots

Consider creating screenshots for README:
- [ ] Screenshot of menu screen
- [ ] Screenshot of question screen
- [ ] Screenshot of game over screen
- [ ] Save as `.png` in `assets/` or `images/` folder

## GitHub Features Setup

### Labels for Issues

Create these labels in your GitHub repository:

| Label | Color | Description |
|-------|-------|-------------|
| bug | Red | Something isn't working |
| enhancement | Green | New feature or improvement |
| documentation | Blue | Documentation updates |
| good-first-issue | Purple | Good for newcomers |
| help-wanted | Yellow | Need assistance |
| question | Orange | Further information needed |
| duplicate | Gray | This issue already exists |

### Issue Templates

Create `.github/ISSUE_TEMPLATE/bug_report.md`:
```markdown
---
name: Bug report
about: Create a report to help us improve
---

## Describe the bug
A clear description of what the bug is.

## To Reproduce
1. ...
2. ...

## Expected behavior
Description of what should happen.

## Screenshots
If applicable, add screenshots.

## Environment
- MATLAB Version: 
- OS: 

## Additional context
Any other context about the problem.
```

## Security Considerations

- [ ] No sensitive information in code (API keys, passwords)
- [ ] No hardcoded file paths with usernames
- [ ] No private data in example files
- [ ] LICENSE file clearly states usage rights
- [ ] No malicious code or dependencies

## Marketing & Visibility

### After Publishing

1. **Announce on Social Media**
   - Twitter/X: "Excited to release Energy Game, an interactive MATLAB educational game about clean energy! 🌍⚡ Check it out on GitHub: [link]"
   - LinkedIn: Professional announcement

2. **Submit to Directories**
   - MATLAB Central File Exchange
   - GitHub Awesome Lists (search "awesome matlab" or "awesome education")
   - Open Source Education platforms

3. **Share with Communities**
   - University/school communities
   - MATLAB user groups
   - Environmental education groups
   - Open source education communities

4. **Add to Your Portfolio**
   - Link from personal website
   - Add to resume/CV
   - Mention in graduate applications

## Post-Publication Maintenance

### Regular Tasks
- [ ] Respond to issues within 1 week
- [ ] Review pull requests
- [ ] Update documentation as needed
- [ ] Release updates regularly
- [ ] Engage with community

### Version Updates
- [ ] Test before creating release
- [ ] Write detailed release notes
- [ ] Tag release on GitHub: `v1.1.0`
- [ ] Update CHANGELOG.md
- [ ] Announce update

## Final Review Checklist

Before pushing to GitHub, verify:

- [ ] All files are included and organized
- [ ] No personal or sensitive information
- [ ] README is clear and complete
- [ ] LICENSE is appropriate
- [ ] All links work correctly
- [ ] Code is tested and working
- [ ] `.gitignore` is configured
- [ ] Commit messages are clear
- [ ] Repository description is set
- [ ] Topics/tags are appropriate

## Deployment Checklist

Final pre-publication:

```bash
# 1. Double-check everything
git status  # Should be "nothing to commit"

# 2. Verify remote
git remote -v
# Should show your GitHub URL

# 3. Final push
git push origin main

# 4. Visit GitHub
# https://github.com/yourusername/energy-game

# 5. Verify all files appear

# 6. Check README displays correctly

# 7. Create first release
# Go to Releases → Create new release → Tag: v1.0.0
```

## Success Criteria

Your GitHub project is ready when:

✅ Repository created and accessible  
✅ All project files uploaded  
✅ README displays and is complete  
✅ LICENSE is included  
✅ At least 10 commits in history  
✅ .gitignore prevents junk files  
✅ CONTRIBUTING.md provides guidelines  
✅ No errors when running project  
✅ Screenshots/examples included  
✅ Issues are labeled and organized  
✅ First release created  
✅ Project is discoverable via search  

---

## Quick Start Commands

```bash
# Navigate to your project
cd ~/energy-game

# Initialize git (if not done)
git init

# Configure git
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"

# Add all files
git add .

# Commit
git commit -m "Initial commit: Energy Game project"

# Add GitHub remote (replace with your URL)
git remote add origin https://github.com/yourusername/energy-game.git

# Push to GitHub
git branch -M main
git push -u origin main

# Create first release (on GitHub website)
# Releases → Create new release → Tag: v1.0.0
```

---

**You're ready to publish! Good luck with your Energy Game project! 🚀**
