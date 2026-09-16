# Energy Game: Clean vs Unclean

An interactive educational game built with MATLAB that teaches players about environmental impacts of different energy sources through engaging gameplay and quiz scenarios. This game was nominated & competed at the Ohio State Fundamentals of Engineering Design Showcase (Fall 2025).

<div align="center">
  <img width="3182" height="2384" alt="FEAU25ShowcaseCandidsArtboard 1 copy 10-100" src="https://github.com/user-attachments/assets/2c1b4136-0a04-44f3-a1df-38810d8b2ca9" />
  <p><em>Photo from the Showcase</em></p>
</div>

<div align="center">
  <img width="434" height="565" alt="image" src="https://github.com/user-attachments/assets/5e628177-a9eb-4e99-af6d-96534d6f1b27" />
  <p><em>Showcase Flyer</em></p>
</div>



## Overview

**Energy Game: Clean vs Unclean** is an educational game that combines puzzle-solving mechanics with environmental science education. Players control characters in a retro-pixel art environment to clean up environmental damage while answering questions about fossil fuels (coal, petroleum) and renewable energy sources (wind energy).

### Game Features

- **Three Progressive Chapters**: Each chapter focuses on a different energy source:
  - Chapter 1: Coal - Environmental impacts and formation
  - Chapter 2: Petroleum - Uses and environmental consequences
  - Chapter 3: Wind Energy - Renewable energy generation and impacts
  
- **Interactive Quiz Gameplay**: Multiple-choice questions with immediate feedback
- **Puzzle Mechanics**: Players use WASD controls to push soap bars across game levels to clean environmental spills
- **Pixel Art Graphics**: Custom sprite-based visuals created with retro game engine aesthetics (Generated using Google Gemini, Cited)
- **Character Dialogue**: Environmental antagonist provides context and hints through narrative

### Technical Stack

- **Language**: MATLAB
- **Graphics Engine**: Custom Simple Game Engine (`simpleGameEngine.m`)
- **Game Framework**: Object-oriented design with MATLAB class system
- **Input Handling**: Keyboard and mouse input support

## Getting Started

### Prerequisites

- MATLAB R2016b or later
- Image Processing Toolbox (for sprite handling)
- No external dependencies required

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/Energy-Game-Clean-vs-Unclean.git
cd Energy-Game-Clean-vs-Unclean
```

2. Add the project to your MATLAB path:
```matlab
addpath(genpath(pwd))
```

3. Run the main game:
```matlab
Final_SDP_Game_By_Mcelhaney_Yang_WithComments
```

### How to Play

1. **Main Menu**: Select "Start" to begin or "Exit" to quit
   - Click buttons with mouse or press 's' to start, 'e' to exit

2. **Game Chapters**: Answer 2 questions per chapter correctly to progress
   - Read the question carefully
   - Select the correct answer by clicking or using arrow keys
   - Incorrect answers require restarting the chapter

3. **Puzzle Levels**: Between questions, push soap bars to clean spills
   - Use WASD keys to move your character
   - Push soap (appearing as white squares) onto spill locations (red spots)
   - Complete all spills to advance to the next question
   - The game tracks dialogue interactions with the CEO antagonist

4. **End Game**: View your success (clean energy future) or restart

### Controls

| Key | Action |
|-----|--------|
| W | Move up |
| A | Move left |
| S | Move down |
| D | Move right |
| Mouse Click | Select menu/quiz options |
| Mouse Click | Select multiple-choice answers |
| ESC | (In some modes) Pause/exit |

## Game Design

### Educational Content

**Chapter 1 - Coal**
- Question 1: Environmental impact of coal burning (acid rain from CO₂ and SO₂ emissions)
- Question 2: Coal formation (compressed carbon-rich plant material)

**Chapter 2 - Petroleum**
- Question 1: Environmental impact of petroleum (greenhouse gases)
- Question 2: Uses of petroleum (fuel for turbines in generators)

**Chapter 3 - Wind Energy**
- Question 1: Negative environmental impacts of wind energy
- Question 2: How wind energy is generated (mechanical rotation produces electricity)

### Gameplay Mechanics

- **Puzzle Solving**: Push mechanic where players must use physics-based collision to move objects to targets
- **Multiple Attempts**: Players can retry failed questions/levels without penalty
- **Progressive Difficulty**: Complexity increases through levels with more spills to clean
- **Feedback System**: Immediate confirmation of correct/incorrect answers with explanatory messages

## Architecture

### simpleGameEngine Class

The core of the project is the `simpleGameEngine` class, which provides:

- **Sprite Management**: Load and display sprite sheets with transparency support
- **Scene Rendering**: Tile-based scene composition with layering support
- **Input Handling**: Unified keyboard and mouse input interface
- **Figure Management**: Efficient MATLAB figure handling with caching

```matlab
% Example usage:
scene = simpleGameEngine('sprite_sheet.png', 16, 16, 8, [0, 0, 0]);
drawScene(scene, background_matrix, foreground_matrix);
key = getKeyboardInput(scene);
[row, col, button] = getMouseInput(scene);
```

### Game Loop Architecture

The main game follows this structure:
1. Initialize game engine and sprite data
2. Main menu loop (awaits user choice)
3. For each chapter:
   - Display quiz question
   - Validate answer (restart if wrong)
   - Run puzzle level with player controls
   - Check completion and advance
4. End game screen (replay/exit)

## Development Notes

### Created by
- **Jonathon Yang**: Game design, graphics, menu/endgame, question implementation
- **Alex McElhaney**: Puzzle game logic, physics/collision system, keyboard input handling

### Asset Attribution
- Pixel art sprites: Custom creation with retro gaming aesthetic
- Game engine framework: Custom MATLAB implementation
- Question content: Original educational material

### Future Improvements

- Add audio/sound effects
- Implement difficulty settings
- Add more levels and questions
- Add achievements/scoring system

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Documentation

- See [docs/DESIGN.md](DESIGN.md) for detailed game design documentation
- See [docs/SDP_Notebook_Group_L_AU_25.pdf](SDP_Notebook_Group_L_AU_25.pdf) for project notes
- See [docs/SDP_Game.pdf](SDP_Game.pdf) for additional game information

## Troubleshooting

### Game won't start
- Ensure all sprite image files (`.png`) are in the correct directory
- Check that MATLAB has access to the project folder
- Verify Image Processing Toolbox is installed: `ver('images')`

### Sprites not displaying
- Confirm sprite sheet dimensions match the values passed to `simpleGameEngine()`
- Check that sprite coordinates in code match actual sprite positions in image file
- Verify PNG files are not corrupted

### Input not responding
- Ensure the game figure window is focused (click on it)
- Check that keyboard/mouse events are not being consumed by other applications
- Try restarting MATLAB

## Contact

For questions, suggestions, or issues:
- Open an issue on GitHub
- Contact me and Alex through the repository

---
