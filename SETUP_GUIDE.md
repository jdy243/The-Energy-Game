# MATLAB Setup Guide

## System Requirements

### Minimum Requirements
- **MATLAB Version**: R2016b or later
- **Operating System**: Windows 7+, macOS 10.12+, Linux (Ubuntu 16.04+)
- **RAM**: 2GB minimum (4GB+ recommended)
- **Disk Space**: 500MB for installation and game files
- **Required Toolbox**: Image Processing Toolbox (for PNG sprite handling)

### Recommended Setup
- **MATLAB Version**: R2020b or later
- **RAM**: 4GB+
- **SSD**: For faster game startup

## Installation Steps

### Step 1: Verify MATLAB Installation

Open MATLAB and check that all required toolboxes are installed:

```matlab
% Check MATLAB version
version

% Verify Image Processing Toolbox
ver('images')
```

If the Image Processing Toolbox is not listed, install it via MATLAB's Add-On Manager.

### Step 2: Clone Repository

```bash
cd C:\Users\YourUsername\Documents  % Windows
cd ~/Documents                        % macOS/Linux

git clone https://github.com/yourusername/Energy-Game-Clean-vs-Unclean.git
cd Energy-Game-Clean-vs-Unclean
```

If you don't have Git installed:
1. Download as ZIP from GitHub
2. Extract to your desired folder

### Step 3: Add Project to MATLAB Path

**Option A: Command Line**

```matlab
% Change to project directory
cd C:\path\to\Energy-Game-Clean-vs-Unclean

% Add all project folders to path
addpath(genpath(pwd))

% Save path for future sessions
savepath
```

**Option B: GUI**
1. In MATLAB, go to **HOME** tab
2. Click **Set Path**
3. Click **Add with Subfolders**
4. Navigate to and select the project folder
5. Click **Save**

### Step 4: Verify Installation

Test that everything is working:

```matlab
% Run basic game startup
try
    % Check if required files exist
    files = {'src/simpleGameEngine.m', 'assets/sprites/Menu.png'};
    for i = 1:length(files)
        if ~isfile(files{i})
            error('Missing file: %s', files{i});
        end
    end
    
    disp('✓ All required files found');
    disp('✓ Installation successful!');
    disp('✓ Ready to run the game');
    
catch ME
    disp('✗ Installation error:');
    disp(ME.message);
end
```

## Running the Game

### Method 1: From Command Window

```matlab
% Make sure you're in the project directory
cd C:\path\to\Energy-Game-Clean-vs-Unclean

% Run the game
Final_SDP_Game_By_Mcelhaney_Yang_WithComments
```

### Method 2: From Editor

1. Open `Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m` in MATLAB Editor
2. Click **Run** (or press Ctrl+Enter)

### Method 3: From File Browser

1. In MATLAB's Current Folder panel, navigate to the project folder
2. Double-click `Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m`

## File Organization for Running

Ensure these files are in the project root or subdirectories are correctly pathed:

```
/
├── src/
│   ├── Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m
│   ├── simpleGameEngine.m
│   ├── SDP_MenuEnd_AND_GameScene.m
│   └── SDP_Menu_Page.m
├── assets/
│   └── sprites/
│       ├── Menu.png
│       ├── Question_1_Page.png
│       ├── Question_2_page.png
│       ├── Question_3_page.png
│       ├── Endgame_Background.png
│       └── (other game sprites)
└── README.md
```

## Troubleshooting

### Problem: "Image Processing Toolbox not installed"

**Solution:**
1. Open MATLAB
2. Click **Add-Ons** in the HOME tab
3. Search for "Image Processing Toolbox"
4. Click **Install**
5. Follow installation wizard

### Problem: "Cannot find file simpleGameEngine.m"

**Solution:**
```matlab
% Check current directory
pwd

% Make sure you're in project folder
cd C:\path\to\Energy-Game-Clean-vs-Unclean

% Re-add path
addpath(genpath(pwd))

% Verify
which simpleGameEngine
```

### Problem: "Sprite images not displaying"

**Possible Causes & Solutions:**

1. **Image files missing**
   ```matlab
   % Check for image files
   cd assets/sprites
   ls *.png  % Unix/Mac
   dir *.png % Windows
   ```

2. **Incorrect image path in code**
   - Verify image filenames match exactly in code
   - Check for case sensitivity issues

3. **Image file corruption**
   - Try re-downloading from repository
   - Verify PNG files open in an image viewer

### Problem: "Keyboard/Mouse input not responding"

**Solutions:**
1. Click on the game figure window to ensure it has focus
2. Check MATLAB isn't in debug mode
3. Restart MATLAB and the game
4. Try on a different keyboard/mouse if available

### Problem: "Game runs slowly"

**Optimization Tips:**
1. Close other MATLAB figures/windows
2. Close other applications consuming resources
3. Ensure you have at least 2GB free RAM
4. On Linux, use `unity` desktop instead of `unity-gnome` for better performance

### Problem: "Cannot run from MATLAB Online"

**Note:** The game requires local graphics rendering and is designed for desktop MATLAB only.

**Solution:** Install MATLAB Desktop version from mathworks.com

## Advanced Configuration

### Running Without Adding to Path

```matlab
% Run directly with full path specification
run('C:\path\to\Energy-Game-Clean-vs-Unclean\src\Final_SDP_Game_By_Mcelhaney_Yang_WithComments.m')
```

### Creating a Launch Script

Create `launch_game.m` in your project root:

```matlab
function launch_game()
    % LAUNCH_GAME Start the Energy Game
    % Ensure path is set and run the game
    
    % Get current script directory
    scriptPath = fileparts(mfilename('fullpath'));
    
    % Add paths
    addpath(genpath(scriptPath));
    
    % Launch game
    Final_SDP_Game_By_Mcelhaney_Yang_WithComments();
end
```

Then run:
```matlab
launch_game
```

### Batch Processing Multiple Instances

```matlab
% Run multiple game instances (for testing)
for i = 1:3
    % Creates separate game instances
    Final_SDP_Game_By_Mcelhaney_Yang_WithComments();
end
```

## Development Setup

### If You're Contributing to the Project

1. Complete basic installation above
2. Fork the repository on GitHub
3. Clone your fork locally
4. Create a feature branch

```bash
git checkout -b feature/your-feature-name
```

5. Set up your editor with MATLAB proper formatting

### Recommended MATLAB Add-Ons for Development

- **SimBiology**: If adding biological simulations
- **Statistics and Machine Learning Toolbox**: For data analysis
- **Signal Processing Toolbox**: For audio (future feature)

Install from MATLAB's Add-On Manager.

## Uninstallation

### Remove from System

1. **MATLAB Path**
   - Open MATLAB Set Path dialog
   - Remove the project folder
   - Click Save

2. **Delete Files**
   ```bash
   # On Windows
   rmdir /s "C:\path\to\Energy-Game-Clean-vs-Unclean"
   
   # On macOS/Linux
   rm -rf ~/path/to/Energy-Game-Clean-vs-Unclean
   ```

## Getting Help

If you encounter issues:

1. **Check this guide** for common solutions
2. **Check GitHub Issues** - your problem may be documented
3. **Search online** - many MATLAB/game development issues are community-documented
4. **File an Issue** on GitHub with:
   - MATLAB version
   - Operating system
   - Error message (full text)
   - Steps to reproduce
   - Screenshots if applicable

## Supported MATLAB Versions

| Version | Support | Notes |
|---------|---------|-------|
| R2015b and earlier | ❌ | Not tested, may not work |
| R2016b | ✓ | Minimum version |
| R2017a-R2018b | ✓ | Fully supported |
| R2019a and later | ✓ | Recommended |
| Latest (R2023b+) | ✓ | Fully supported |

## Next Steps

After successful installation:

1. Read the [README.md](../README.md) for gameplay instructions
2. Check [DESIGN.md](DESIGN.md) for technical details
3. Look at example scripts in `/examples/` folder
4. Start playing and enjoy! 🎮

---

**Last Updated**: 2024
**Guide Version**: 1.0
