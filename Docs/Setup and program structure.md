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



