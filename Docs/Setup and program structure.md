# SETUP AND PROGRAM STRUCTURE

## 1. Godot Project
- is a folder containing:
1. ```project.godot```: main config file
2. Scene files ```.tscn```: game objects/levels
3. Script files ```.gd```: codebase
4. Assets
5. Auto-generated files ```.import```,```.uid```

- ```res://``` means the root of your project folder

## 2. Recommended Folder Structure

```
MyGame/
├── project.godot          # Main project file (DON'T EDIT MANUALLY)
├── .gitignore            # Git ignore rules
├── README.md             # Project description
│
├── scenes/               # All scene files (.tscn)
│   ├── main.tscn
│   ├── player.tscn
│   ├── enemy.tscn
│   └── ui/
│       └── menu.tscn
│
├── scripts/              # All GDScript files (.gd)
│   ├── main.gd
│   ├── player.gd
│   └── enemy.gd
│
├── assets/               # All game assets
│   ├── images/
│   │   ├── sprites/
│   │   └── backgrounds/
│   ├── sounds/
│   │   ├── music/
│   │   └── sfx/
│   └── fonts/
│
└── docs/                 # Personal notes/documentation
    └── learning_notes.md

```

## 3. Important files
1. ```project.godot```
- main config file
- contains: projects settings, display sze, input mappings, enables plugins

2. ```.import```
- cache for imported assets
- optimized versions of your images/sounds
- don't add to git(add to .gitignore)
- auto-generated

3. ```.tscn```
- a scene (collection of nodes)
- format: text-based
- contains: node hierarchy, properties, references to scripts

4. ```.gd```
- GDScript code
- format:plain text
- contains game logic

5. ```.uid```
- Unique identities for files
- not to be 


## 4. Starting a project

### Step 1: Create project in Godot
1. Open Godot
2. Click "New Project"
3. Choose name and location
4. Select "Forward+" renderer
5. Click "Create & Edit"

### Step 2: Create folder structure immediately In Godot's FileSystem panel:
- at the bottom left panel
Right-click res:// → New Folder → "scenes"
Right-click res:// → New Folder → "scripts"
Right-click res:// → New Folder → "assets"
Right-click assets → New Folder → "images"
Right-click assets → New Folder → "sounds"

### Step 3: Setup Git

```bash
cd /mnt/c/Users/YourName/path/to/project
git init
# Create .gitignore (see above)
git add .
git commit -m "initial project setup"
git remote add origin <your-repo-url>
git push -u origin main
```

**Step 4: Create your first scene in the right place**
```
1. Right-click scenes/ folder → "New Scene"
2. Select "2D Scene"
3. Save as "scenes/main.tscn"
4. Attach script → save to "scripts/main.gd"
```

---

## 6. File Naming Conventions

### Scenes (`.tscn`)
- Use snake_case: `main_menu.tscn`, `player_character.tscn`
- Be descriptive: `enemy_goblin.tscn` not `enemy1.tscn`
- Save in `scenes/` folder

### Scripts (`.gd`)
- Match the scene name: `player_character.gd` for `player_character.tscn`
- Or describe function: `game_manager.gd`, `score_tracker.gd`
- Save in `scripts/` folder

### Assets
- Use descriptive names: `player_idle.png`, `coin_collect.wav`
- Group by type in subfolders
- Keep organized from the start

---

## 7. Working with Multiple Scenes

### Scene Organization
```
scenes/
├── main.tscn              # Main game scene
├── characters/
│   ├── player.tscn
│   └── enemy_goblin.tscn
├── levels/
│   ├── level_1.tscn
│   └── level_2.tscn
└── ui/
    ├── main_menu.tscn
    └── hud.tscn

```

## 8. Project Settings You Should Know
Access via: Project → Project Settings

Important Settings:
1. Display:
- Window width/height (e.g., 1920x1080)
- Stretch mode (how game scales on different screens)

2. Input Map:

Define controls (W/A/S/D, arrow keys, etc.)
We'll use this when learning user input

3. Physics:

Gravity, collision layers
Default settings are usually fine


9. Best Practices
DO:
✅ Create folder structure BEFORE building
✅ Name files descriptively
✅ Commit to Git regularly
✅ Keep one script per scene when starting
✅ Organize assets by type
✅ Use res:// paths in code
DON'T:
❌ Put everything in root folder
❌ Edit .import/ or .uid files
❌ Edit project.godot manually
❌ Use spaces in file names (use snake_case)
❌ Forget to save scenes after changes

10. Common Beginner Mistakes
Mistake 1: Not organizing from the start
Problem: Files everywhere, hard to find things
Solution: Create scenes/, scripts/, assets/ folders immediately
Mistake 2: Moving files manually in file explorer
Problem: Breaks references, scripts stop working
Solution: Always move files in Godot's FileSystem panel (right-click → Move/Rename)
Mistake 3: Forgetting to save
Problem: Changes don't persist
Solution: Always Ctrl+S after editing scenes or scripts
Mistake 4: Not using Git
Problem: Can't undo mistakes, lose work
Solution: Commit frequently









