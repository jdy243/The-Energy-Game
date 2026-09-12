# Energy Game: Clean vs Unclean 🌍⚡

An interactive MATLAB-based educational game that teaches players about clean energy, fossil fuels, and environmental impacts through an engaging gamified experience.

![Game Banner](images/Menu_Background.png)

## 📋 Overview

**Energy Game** is an educational puzzle game designed to help students understand:
- Environmental impacts of different energy sources (coal, petroleum, wind)
- The difference between clean and unclean energy
- Origins and uses of various energy resources
- Environmental consequences through visual feedback

The game features:
- **Interactive quiz-style questions** on energy and environment topics
- **Visual learning** with retro-style pixel art graphics
- **Multiple question types** covering coal, petroleum, and renewable energy
- **Score tracking** with CO₂ reduction and renewable energy share metrics
- **Game-over scenarios** showing outcomes of player choices

## 🎮 Gameplay

### Game Flow
1. **Menu Screen** - Select to start the game
2. **Question Screens** - Answer multiple-choice questions about energy
3. **Game Over Screen** - View results and replay or exit

### Questions Include
- Environmental impacts of coal and petroleum
- Energy sources and their origins
- Renewable energy mechanisms
- How energy is used in daily life

## 🛠️ Requirements

- **MATLAB** R2023b or later
- **Image Processing Toolbox** (for sprite rendering)
- **retro_pack.png** - Sprite sheet asset (included)
- **Menu.png** - Menu background asset (included)

### Supported Platforms
- Windows 10/11
- macOS (Intel & Apple Silicon)
- Linux (Ubuntu 20.04+)

## 📦 Installation

### Option 1: Clone from GitHub
```bash
git clone https://github.com/yourusername/energy-game.git
cd energy-game
```

### Option 2: Download ZIP
Download the repository as ZIP and extract to your desired location.

## ▶️ Running the Game

1. Open MATLAB
2. Navigate to the project directory
3. Run the main game file:
   ```matlab
   Final_SDP_Game_By_Mcelhaney_Yang_WithComments
   ```

## 📁 Project Structure

```
energy-game/
├── Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m    # Main game logic
├── simpleGameEngine.m                                  # Game engine foundation
├── SDP_Menu_Page.m                                     # Menu screen logic
├── SDP_MenuEnd_AND_GameScene.m                        # Game scenes
├── SDP_Preview.m                                       # Game preview/setup
├── Mathslime.m                                         # Utility functions
├── assets/
│   ├── Menu.png                                        # Menu background
│   └── retro_pack.png                                  # Sprite sheet
├── README.md                                           # Project documentation
├── LICENSE                                             # MIT License
└── CONTRIBUTING.md                                     # Contribution guidelines
```

## 🎯 Features

### Current Features
- ✅ 3 multiple-choice questions on energy topics
- ✅ Retro pixel art graphics
- ✅ Score tracking (CO₂ reduction, renewable energy share)
- ✅ Game-over screen with final statistics
- ✅ Replay functionality
- ✅ Clean and unclean energy scenarios

### Planned Features
- 🔜 Additional question categories
- 🔜 Difficulty levels
- 🔜 Leaderboard system
- 🔜 Custom game modes
- 🔜 Save/load game state

## 🎓 Learning Outcomes

After playing this game, students will understand:
- The environmental consequences of fossil fuel usage
- The benefits of renewable energy sources
- How energy sources differ in origin and impact
- The relationship between energy choices and climate change

## 👥 Contributors

### Project Team
- **Jonathan Yang** - Game design, UI/UX, graphics, questions, mouse input handling
- **Alex** - Puzzle game logic, keyboard input, game mechanics

Special thanks to the Simple Game Engine community for the sprite rendering framework.

## 🤝 Contributing

We welcome contributions! Here's how you can help:

### For Bug Reports
1. Open an issue with a clear title and description
2. Include steps to reproduce the bug
3. Specify your MATLAB version and OS

### For New Features
1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Make your changes with descriptive comments
4. Test thoroughly
5. Submit a pull request with a clear description

### Coding Standards
- Use descriptive variable names
- Add comments for complex logic
- Keep functions modular and reusable
- Follow MATLAB naming conventions (camelCase for variables, PascalCase for functions)

See [CONTRIBUTING.md](CONTRIBUTING.md) for detailed guidelines.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

### What you can do:
- ✅ Use commercially
- ✅ Modify the code
- ✅ Distribute
- ✅ Use privately

### You must:
- 📋 Include the original license and copyright notice

## 🐛 Known Issues

- [ ] Issue #1: [Describe any known issues here]
- [ ] Issue #2: [When fixed, remove from this list]

## 📝 Changelog

### Version 1.0.0 (2026-09-12)
- Initial release
- Core gameplay mechanics
- 3 question sets
- Menu and game-over screens
- Score tracking

## 🔗 Links

- **Documentation**: See [SDP_Game.pdf](docs/SDP_Game.pdf)
- **Sprite Assets**: Generated from retro_pack.png
- **Issue Tracker**: [GitHub Issues](../../issues)
- **Discussions**: [GitHub Discussions](../../discussions)

## 💡 Tips for Educators

This game can be used in:
- Environmental science classes
- Energy and sustainability courses
- STEM education programs
- Computer science (MATLAB introduction)

Consider pairing the game with:
- Discussion on climate change
- Research on renewable energy
- Policy analysis on energy regulations

## 📧 Contact & Support

- Report bugs via [GitHub Issues](../../issues)
- Start a discussion in [GitHub Discussions](../../discussions)
- Email: your.email@example.com

## 🙏 Acknowledgments

- MATLAB community for the Simple Game Engine
- Students who playtested and provided feedback
- Environmental scientists for accurate information

---

**Made with ❤️ by the Energy Game Team**

*Last Updated: September 2026*
