# Contributing to Energy Game

Thank you for your interest in contributing to the Energy Game project! We welcome contributions from students, educators, and developers.

## Code of Conduct

Please be respectful and constructive in all interactions. We're building this project together!

## How to Contribute

### 1. Reporting Bugs

If you find a bug, please:

1. **Check existing issues** to avoid duplicates
2. **Create a new issue** with:
   - **Title**: Clear, descriptive summary
   - **Description**: What you were doing when the bug occurred
   - **Steps to reproduce**: Step-by-step instructions
   - **Expected behavior**: What should happen
   - **Actual behavior**: What actually happened
   - **Screenshots**: If applicable
   - **Environment**:
     - MATLAB version
     - Operating System
     - Toolboxes installed

**Example:**
```
Title: Game crashes when answering the petroleum question

Description: The game crashes immediately after selecting answer B 
for the petroleum question on question 2.

Steps to reproduce:
1. Start the game
2. Answer the coal question correctly
3. Answer any option for the petroleum question about environmental impacts
4. Click answer B
5. Game crashes

Expected: Move to next question
Actual: MATLAB error dialog appears

Environment: MATLAB 2024a, Windows 11, Image Processing Toolbox installed
```

### 2. Suggesting Enhancements

Have an idea to improve the game? We'd love to hear it!

1. **Describe your enhancement** with:
   - **Clear use case**: Who would benefit?
   - **Proposed solution**: How would it work?
   - **Alternative approaches**: Other ways to solve this?
   - **Related issues**: References to related issues

**Example:**
```
Title: Add difficulty levels to the game

Description: Students with different knowledge levels need different challenges.

Proposal: Add three difficulty modes:
- Easy: 3 basic questions
- Medium: 5 intermediate questions (current)
- Hard: 7 advanced questions with timed responses

This would make the game more engaging for diverse classrooms.
```

### 3. Code Contributions

#### Getting Started

1. **Fork the repository**
   ```bash
   # On GitHub, click "Fork" button
   ```

2. **Clone your fork**
   ```bash
   git clone https://github.com/YOUR-USERNAME/energy-game.git
   cd energy-game
   ```

3. **Create a feature branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or for bug fixes:
   git checkout -b fix/bug-description
   ```

4. **Make your changes**
   - Keep changes focused and atomic
   - Write clear commit messages
   - Test your code thoroughly

5. **Commit your changes**
   ```bash
   git add .
   git commit -m "Clear description of changes"
   ```

6. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**
   - Describe what you changed and why
   - Link related issues (use `Closes #123`)
   - Explain any breaking changes

#### MATLAB Coding Standards

Please follow these conventions:

**Naming:**
- Variables: `camelCase` → `playerScore`, `currentQuestion`
- Functions: `functionName()` → `drawBackground()`, `checkAnswer()`
- Constants: `CONSTANT_NAME` → `MAX_PLAYERS`, `GAME_WIDTH`
- Private functions: `private_function_name()` → `load_sprite_data()`

**Style:**
```matlab
% Good: Clear comments and spacing
function [result] = calculateScore(correct, total)
    % CALCULATECORE Computes the player's score percentage
    %
    % Input:
    %   correct (int): Number of correct answers
    %   total (int): Total number of questions
    %
    % Output:
    %   result (double): Score as percentage (0-100)
    
    result = (correct / total) * 100;
end

% Avoid: Unclear variable names and missing documentation
function z = f(x, y)
    z = (x / y) * 100;
end
```

**Comments:**
```matlab
% Use full sentences with proper grammar
% Explain WHY, not just WHAT the code does

% Calculate damage with 20% random variance
baseDamage = 50;
variance = 0.2;
finalDamage = baseDamage * (1 + rand() * variance);

% Avoid obvious comments
% i = i + 1  % increment i ← DON'T do this
```

**File Organization:**
```matlab
%--------------------------------------------------------------------------
% FUNCTION_NAME Summary of what this function does
%--------------------------------------------------------------------------
% Description: Detailed explanation
%
% Inputs:
%   param1 - Description and type
%   param2 - Description and type
%
% Outputs:
%   output1 - Description and type
%
% Examples:
%   result = myFunction(10, 20);
%
% Author: Name
% Last Modified: YYYY-MM-DD
%--------------------------------------------------------------------------

function [output] = myFunction(param1, param2)
    % Implementation here
end
```

### 4. Documentation Improvements

Help us improve documentation!

- **Fix typos** in README or comments
- **Improve clarity** of existing documentation
- **Add examples** for complex features
- **Translate** documentation to other languages

Steps:
1. Fork the repository
2. Make your documentation changes
3. Submit a pull request with description

### 5. Adding Questions

Want to add new educational questions? Great!

**Submit via Issue:**

1. Open an issue titled: "Question: [Topic Name]"
2. Include:
   - Question text
   - 4 multiple choice answers
   - Correct answer
   - Explanation of why it's correct
   - Educational relevance
   - Difficulty level (easy/medium/hard)

**Format:**
```
**Question:** What is renewable energy?

**Options:**
A. Energy from fossil fuels
B. Energy from natural resources that replenish
C. Energy stored in batteries
D. Energy used by industries only

**Correct Answer:** B

**Explanation:** Renewable energy comes from natural resources like solar, wind, 
and water that naturally replenish and are sustainable.

**Relevance:** Teaches students about clean energy sources

**Difficulty:** Easy
```

### 6. Testing

Before submitting a pull request:

1. **Test on your system**
   ```matlab
   % Run the game and play through
   Final_SDP_Game_By_Mcelhaney_Yang_WithComments
   ```

2. **Test different scenarios**
   - Try different answer combinations
   - Test on different MATLAB versions if possible
   - Check for any error messages or crashes

3. **Document test results** in your PR

## Pull Request Process

1. **Update documentation** (README, CONTRIBUTING, etc.) if needed
2. **Test thoroughly** on your system
3. **Write clear commit messages**
4. **Create descriptive pull request**
5. **Wait for review** - maintainers will provide feedback
6. **Address feedback** - make requested changes
7. **Get approved** - once approved, maintainer will merge

### PR Template:

```markdown
## Description
Clear description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Documentation update
- [ ] Code improvement

## Related Issues
Closes #123

## Testing
How to test these changes

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-reviewed changes
- [ ] Added comments
- [ ] Updated documentation
- [ ] Tested thoroughly
```

## Project Structure for Contributors

```
energy-game/
├── Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m   ← Main game logic
├── simpleGameEngine.m                                ← Game engine
├── assets/                                            ← Images, sprites
├── docs/                                              ← Documentation
├── tests/                                             ← Test files
└── README.md                                          ← Project overview
```

## Getting Help

- **Issues**: Ask questions in issue discussions
- **Discussions**: Use GitHub Discussions for ideas
- **Email**: contact developers for urgent issues

## Recognition

Contributors will be:
- Added to the CONTRIBUTORS.md file
- Mentioned in release notes
- Recognized in the README

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

## Questions?

Don't hesitate to ask! Open an issue or start a discussion.

---

**Thank you for helping make Energy Game better! 🎮🌍**
