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








