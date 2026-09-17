# Contributing to Energy Game: Clean vs Unclean

Thank you for your interest in contributing to our project! We welcome contributions from everyone. This document provides guidelines and instructions for contributing.

## Code of Conduct

Be respectful, inclusive, and constructive in all interactions. We're building this for educational purposes and want to maintain a positive community.

## How to Contribute

### Reporting Bugs

Before creating a bug report, check if the issue already exists. When creating a bug report, include:

- **Title**: Clear, descriptive title
- **Description**: What you were doing when the bug occurred
- **Expected behavior**: What should have happened
- **Actual behavior**: What actually happened
- **Steps to reproduce**: Detailed steps to reproduce the issue
- **Environment**: MATLAB version, operating system, any relevant configurations
- **Screenshots**: If applicable, include screenshots or recorded gameplay

### Suggesting Enhancements

Enhancement suggestions are welcome. When suggesting an enhancement:

- Use a clear, descriptive title
- Provide a detailed description of the suggested enhancement
- Include use cases and examples
- Explain why this enhancement would be useful for players

### Pull Requests

1. **Fork the repository** on GitHub

2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/your-username/Energy-Game-Clean-vs-Unclean.git
   cd Energy-Game-Clean-vs-Unclean
   ```

3. **Create a feature branch** from `main`:
   ```bash
   git checkout -b feature/your-feature-name
   ```

4. **Make your changes**:
   - Follow the coding standards (see below)
   - Make commits with clear, descriptive messages
   - Keep commits focused and atomic
   - Reference relevant issues in commit messages

5. **Test your changes**:
   - Test in MATLAB R2016b and later versions if possible
   - Verify game mechanics work as expected
   - Check that no existing features are broken

6. **Push to your fork**:
   ```bash
   git push origin feature/your-feature-name
   ```

7. **Create a Pull Request**:
   - Write a clear PR title and description
   - Reference any related issues (#123)
   - Include screenshots/videos if UI changes were made
   - Wait for review and address any feedback

## Coding Standards

### MATLAB Style Guide

- **Indentation**: Use 4 spaces (not tabs)
- **Line length**: Keep lines under 100 characters when possible
- **Variable names**: Use camelCase for variables and functions
- **Class names**: Use PascalCase
- **Comments**: Use `%` for single-line comments and `%{` `%}` for multi-line blocks
- **Function documentation**: Include doc comments describing purpose, inputs, and outputs

Example:
```matlab
function output = exampleFunction(input1, input2)
    % EXAMPLEFUNCTION Brief description of what this does.
    %
    % Detailed explanation of the function's behavior.
    %
    % Inputs:
    %   input1 - Description of input1
    %   input2 - Description of input2
    %
    % Outputs:
    %   output - Description of output
    %
    % Example:
    %   result = exampleFunction(value1, value2);
    
    % Your code here
    output = input1 + input2;
end
```

### Code Organization

- Keep functions focused and single-purpose
- Use meaningful variable names
- Add comments for complex logic
- Organize related code into classes or modules
- Maintain consistent structure across game scenes

### Git Commit Messages

Follow this format:

```
[Type] Brief description (50 chars or less)

Longer explanation if needed (72 chars or less per line)

- Bullet point if explaining multiple changes
- Reference issue: Fixes #123
```

Types:
- `[Feature]` - New feature
- `[Fix]` - Bug fix
- `[Refactor]` - Code refactoring without feature changes
- `[Docs]` - Documentation updates
- `[Test]` - Adding or updating tests
- `[Style]` - Code style changes

Example:
```
[Feature] Add difficulty settings to gameplay

Implements three difficulty levels (Easy, Medium, Hard) that adjust:
- Number of spills to clean
- Time limit for questions
- Number of hints available

Fixes #45
```

## Project Structure Conventions

When adding new files:

- **Game logic**: `src/` directory
- **Level definitions**: `levels/` directory (if adding new levels)
- **Assets**: `assets/` subdirectories by type (sprites, audio, etc.)
- **Documentation**: `docs/` directory
- **Tests**: `tests/` directory

## Testing

If you add new features:

1. Test in MATLAB on your system
2. Verify existing games still work
3. Test with different sprite sets if applicable
4. Document any new dependencies

## Documentation

- Update README.md if adding features
- Add comments to complex code sections
- Update DESIGN.md if changing game architecture
- Include examples for new public functions

## Areas We Need Help With

- **Bug fixes**: Review open issues and help fix bugs
- **New levels**: Design and implement new game levels
- **Educational content**: Improve or add quiz questions
- **Graphics**: Create new sprite assets
- **Accessibility**: Improve UI for players with disabilities
- **Localization**: Translate to other languages (starting with base English)
- **Documentation**: Improve guides and API documentation
- **Testing**: Test on different MATLAB versions and systems

## Licensing

By contributing to this project, you agree that your contributions will be licensed under the MIT License.

## Questions?

- Check existing documentation and issues first
- Open a new GitHub discussion
- Contact the maintainers through GitHub

## Recognition

Contributors will be recognized in:
- README.md (All Contributors section)
- Release notes for their contributions
- GitHub's contributor page

---

Thank you for helping make Energy Game: Clean vs Unclean better!
