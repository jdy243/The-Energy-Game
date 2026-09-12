# Energy Game: Design Documentation

## Project Overview

Energy Game: Clean vs Unclean is an educational puzzle-quiz hybrid game designed to teach players about fossil fuels and renewable energy sources through interactive gameplay.

## Game Design

### Core Concept

The game combines two gameplay mechanics:
1. **Quiz/Educational Component**: Multiple-choice questions about energy sources
2. **Puzzle/Action Component**: Physics-based pushing puzzles where players clean environmental spills

This hybrid approach keeps the game engaging while delivering educational content.

### Learning Objectives

By completing this game, players will understand:

- **Coal (Chapter 1)**
  - How coal is formed (ancient plant material compressed under heat and pressure)
  - Environmental impacts of coal combustion (sulfur dioxide causing acid rain, carbon dioxide emissions)

- **Petroleum (Chapter 2)**
  - Uses of petroleum (fuel for power generation, transportation)
  - Environmental impacts (greenhouse gases from combustion)
  - How petroleum relates to human infrastructure

- **Wind Energy (Chapter 3)**
  - How wind energy works (wind turns turbines which generate electricity)
  - Understanding that renewable energy has tradeoffs (some environmental impact)
  - Comparing different energy sources

### Gameplay Flow

```
START
  ↓
[MAIN MENU] - Player selects Start or Exit
  ↓ (Start selected)
[CHAPTER 1: COAL] 
  ├─ QUIZ QUESTION 1
  │  ├─ Correct → Proceed
  │  └─ Incorrect → Retry
  ├─ CLEANUP PUZZLE 1
  └─ QUIZ QUESTION 2
     ├─ Correct → Proceed
     └─ Incorrect → Retry
  ↓
[CHAPTER 2: PETROLEUM]
  ├─ QUIZ QUESTION 3
  ├─ CLEANUP PUZZLE 2
  └─ QUIZ QUESTION 4
  ↓
[CHAPTER 3: WIND ENERGY]
  ├─ QUIZ QUESTION 5
  ├─ CLEANUP PUZZLE 3
  └─ QUIZ QUESTION 6
  ↓
[END GAME SCREEN]
  ├─ Clean Energy Future (success path)
  ├─ Replay button
  └─ Exit button
  ↓
END
```

## Game Mechanics

### Quiz Mechanic

**Question Presentation**
- Question displayed in text box at top of screen
- Four multiple-choice answers presented as clickable buttons
- Accompanying environment-themed pixel art (coal factory, oil platform, wind turbines)

**Answer Validation**
- Player clicks on chosen answer
- Immediate visual feedback (highlight on selection)
- System checks correctness
  - **Correct**: Advancement text plays, move to next phase
  - **Incorrect**: Retry message, question re-presented

**Design Rationale**
- Multiple choice keeps learning linear and focused
- Immediate feedback aids learning
- Three questions per energy source ensures comprehensive coverage
- Player must get questions right - reinforces learning

### Puzzle Mechanic

**Objective**
- Clean environmental spills by pushing "soap" objects to "spill" locations
- Player controls a character with WASD keys
- Pushes soap bars across a tile-based map

**Mechanics**
- **Movement**: WASD keys move character one tile at a time
- **Pushing**: Walking into soap pushes it in that direction (momentum-based)
- **Collision**: Character cannot walk through walls or obstacles
- **Win Condition**: All spill locations have soap on top of them

**Level Design**
Each level has:
- Open areas with soap objects and spill locations
- Walls and obstacles that create challenging paths
- Multiple spills to create varied puzzle difficulty
- Grid-based tile system for predictable movement

**Design Rationale**
- Gives visual/mechanical representation of "cleaning up" environmental damage
- Provides pacing break from quiz questions
- Physics-based pushing is satisfying and encourages engagement
- Tile-based movement is easy to control and design

### Difficulty Progression

The game has implicit difficulty progression:
1. **Chapter 1**: Simple quizzes, easy puzzle
2. **Chapter 2**: More complex questions, medium puzzle  
3. **Chapter 3**: Challenging concept questions, complex puzzle

Players can retry as many times as needed - no failure penalty, only learning opportunity.

## Technical Architecture

### Core Components

#### simpleGameEngine Class

The foundation of all visuals and input.

```matlab
simpleGameEngine(spritePath, tileWidth, tileHeight, spriteCount, colorKey)
```

**Responsibilities:**
- Load sprite sheets from PNG files
- Render scenes from tile maps
- Handle keyboard input
- Handle mouse input
- Manage MATLAB figure/axes

**Key Methods:**
- `drawScene(background, foreground)` - Render game scene
- `getKeyboardInput()` - Poll for key presses
- `getMouseInput()` - Get mouse position and click status

#### Game State Manager

Tracks:
- Current chapter (1, 2, or 3)
- Current scene (menu, quiz, puzzle, end)
- Player progress (which questions passed)
- Quiz answer correctness

#### Quiz System

`handleQuizScene()` manages:
- Question display
- Answer collection
- Correctness validation
- Transition logic

#### Puzzle System

`handlePuzzleScene()` manages:
- Game state initialization
- Player movement input
- Collision detection
- Win condition checking
- Sprite updates

### Data Structures

#### Sprite Mapping

Sprites are organized in a sheet with standard indices:
```
Index -> Sprite Type
0-3   -> Ground tiles
4-7   -> Wall tiles
8-11  -> Character sprite
12    -> Soap object
13    -> Spill location
14+   -> Special tiles
```

#### Level Maps

2D matrices representing game levels:
```matlab
background = [
    1 1 1 1 1 1;
    1 0 0 0 0 1;
    1 0 12 13 0 1;  % 12=soap, 13=spill
    1 0 0 0 0 1;
    1 1 1 1 1 1;
];
```

#### Question Data

Questions stored as structs:
```matlab
question = struct(...
    'text', 'Question text here',...
    'answers', {'Option A', 'Option B', 'Option C', 'Option D'},...
    'correct', 2 ...  % Index of correct answer (1-4)
);
```

## Content Design

### Chapter 1: Coal

**Educational Focus**: Formation and environmental impact

**Question 1**: "What is one environmental impact of using coal?"
- Options explore different impacts (acid rain, ozone layer, water vapor, toxin neutralization)
- Correct answer: Acid rain from SO₂ emissions
- Key concept: Coal produces pollutants when burned

**Question 2**: "Where does coal come from?"
- Options explore origin theories (plant material, crystallized minerals, shells, metal reactions)
- Correct answer: Compressed ancient plant material
- Key concept: Coal is fossilized organic matter

**Visual Theme**: Industrial factory with smoke stacks, underground mining

### Chapter 2: Petroleum

**Educational Focus**: Uses and environmental impact

**Question 1**: "What is one environmental impact of using petroleum?"
- Options explore impacts (ozone healing, soil fertility, greenhouse gases, wildlife growth)
- Correct answer: Greenhouse gases
- Key concept: Petroleum combustion produces climate-affecting emissions

**Question 2**: "What is one way we use petroleum?"
- Options explore uses (solar panels, fuel, fertilizer, wood products)
- Correct answer: Fuel (for power generation)
- Key concept: Petroleum is critical infrastructure resource

**Visual Theme**: Oil refinery with cranes, coastal industrial setting, environmental spill

### Chapter 3: Wind Energy

**Educational Focus**: Renewable energy mechanics and tradeoffs

**Question 1**: "What is one negative environmental impact of using wind energy?"
- Options explore impacts (ozone depletion, soil degradation, water pollution, none of above)
- Correct answer: None of the above (wind energy has minimal environmental impact)
- Key concept: Even renewable energy must be evaluated holistically

**Question 2**: "How is wind energy generated?"
- Options explore mechanisms (air turns turbines, sun heats water, fossil fuels burned, water wheels)
- Correct answer: Moving air turns turbines
- Key concept: Wind energy conversion to electricity

**Visual Theme**: Wind turbine farm, green landscape with wildlife, clean energy aesthetic

## Art Direction

### Visual Style

- **Retro Pixel Art**: 8-16 bit era aesthetic
- **Color Palette**: 
  - Greens: Environmental/clean energy themes
  - Grays/Browns: Industrial/fossil fuel themes
  - Blues: Water and sky
  - Bright accents: UI and interactive elements

### Sprite Design

- **Characters**: Pixel avatars representing "players" cleaning up (space suit, factory uniform)
- **Obstacles**: Recognizable pixel art for walls, soap, spills
- **Backgrounds**: Thematic environments for each chapter

### UI Design

- **Menu**: Large readable text with highlighted buttons
- **Quiz**: Question box with four distinct answer buttons
- **Puzzle**: Minimal UI, focus on gameplay
- **End Screen**: Large success/failure message with next action buttons

## Accessibility Considerations

### Current Implementation
- High contrast UI text and backgrounds
- Clear answer labels
- Keyboard and mouse input support

### Future Improvements
- Add color-blind friendly palettes
- Add sound/visual effects for feedback
- Add adjustable text sizing
- Add controller support

## Educational Pedagogy

### Learning Theory Foundation

The game uses several learning principles:

1. **Active Learning**: Players engage through quiz selection and puzzle solving
2. **Immediate Feedback**: Correct/incorrect answers immediately apparent
3. **Scaffolding**: Difficulty increases gradually across chapters
4. **Contextualization**: Questions tied to visual representations
5. **Engagement**: Game format maintains attention

### Content Accuracy

All questions and answers are factually accurate regarding:
- Energy science (formation, conversion, use)
- Environmental impact (confirmed through scientific literature)
- Current energy technology

## Performance Considerations

### Target Specifications
- MATLAB R2016b and later
- Any modern computer (Windows, Mac, Linux)
- No significant GPU requirements
- Figure rendering only (no complex graphics engine)

### Optimization
- Sprite caching reduces file I/O
- Minimal scene updates per frame
- Simple collision detection algorithms
- Tile-based rendering is efficient

## Extensibility

### Adding New Chapters

To add a new chapter:

1. Create new question structs (minimum 2 questions)
2. Design and create puzzle level layout
3. Add sprite art for the theme
4. Integrate into main game flow loop
5. Update documentation

### Adding New Levels

Each chapter can have multiple cleanup puzzles:
1. Design level layout as tile matrix
2. Adjust soap/spill positions
3. Adjust difficulty (more spills, complex paths)
4. Test in game loop

### Modifying Content

Questions and answers can be easily modified in the question data structs without code changes.

## Known Limitations

1. **MATLAB-only**: Requires MATLAB license (cannot be distributed as standalone)
2. **Performance**: Slower rendering than native game engines
3. **Graphics**: Limited to MATLAB's figure capabilities
4. **Audio**: Currently no sound support in MATLAB version
5. **Save/Load**: No persistent game saves implemented

## Future Enhancement Ideas

### Gameplay Expansions
- More chapters on other energy sources (solar, hydroelectric, nuclear, geothermal)
- Difficulty settings (Easy/Medium/Hard)
- Achievement system with scoring
- Multiplayer quiz mode
- Time limits for additional challenge

### Technical Improvements
- Port to game engine (Unity, Unreal, Godot)
- Add sound effects and music
- Add animation to characters and UI
- Implement save/load game state
- Add controller input support
- Create level editor tool

### Educational Enhancements
- Add more detailed explanations
- Include videos or animations
- Add quiz statistics tracking
- Create teacher guides and materials
- Add multiple language support

### Distribution
- Package as standalone executable (using MATLAB compiler)
- Deploy web version (JavaScript port)
- Create mobile versions (iOS/Android)
- Add to educational game platforms

## Version History

### v1.0 (Current)
- Initial release
- Three chapters (coal, petroleum, wind energy)
- Quiz and puzzle mechanics
- Menu and end game screens
- Pixel art visual theme

---

**Design Document Last Updated**: 2024
**Game Version**: 1.0.0
