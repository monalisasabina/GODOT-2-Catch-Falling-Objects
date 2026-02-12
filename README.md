# Catch the Falling Objects - Learning Project

A simple 2D game built while learning Godot fundamentals. Objects fall from the top of the screen and the player catches them.

## 🎯 Learning Goals

This project covers Phase 1 fundamentals:
- ✅ Setup & Project structure
- ✅ Nodes & Scene system
- 🔄 Basic GDScript syntax
- 🔄 Movement & `_process()`
- ⏳ User input (keyboard/mouse)
- ⏳ Collisions (detecting when things hit)
- ⏳ Spawning/deleting nodes dynamically
- ⏳ Timers & signals

## 🎮 Game Concept

- Player moves left/right at the bottom of the screen
- Objects fall from the top
- Catch objects to score points
- Miss objects to lose lives
- Game over when lives reach 0

## 🛠️ Tech Stack

- **Engine:** Godot 4.6
- **Language:** GDScript
- **Platform:** Windows (exportable to others)
- **Version Control:** Git + GitHub

## 📁 Project Structure
```
catch-falling-objects/
├── project.godot          # Main project file
├── .gitignore            # Git ignore rules
├── README.md             # This file
│
├── scenes/               # Scene files (.tscn)
│   ├── main.tscn        # Main game scene
│   ├── player.tscn      # Player character
│   └── enemy.tscn       # Enemy/practice scene
│
├── scripts/              # GDScript files (.gd)
│   ├── main.gd
│   ├── player.gd
│   └── enemy.gd
│
├── assets/               # Game assets
│   └── images/
│       └── icon.svg     # Godot default icon
│
└── docs/                 # Learning notes & documentation
    └── learning_notes.md
```

## 🚀 Getting Started

### Prerequisites
- Godot 4.6 installed
- Git installed (optional but recommended)

### Setup
1. Clone this repository:
```bash
   git clone <your-repo-url>
```

2. Open Godot and import the project:
   - Click "Import"
   - Navigate to project folder
   - Select `project.godot`
   - Click "Import & Edit"

3. Run the project:
   - Press `F5` or click the ▶ play button

## 📚 Key Concepts Learned

### Nodes
- Single building blocks (Sprite2D, CharacterBody2D, etc.)
- Each node has one specific job
- Organized in parent-child trees

### Scenes
- Saved collections of nodes (.tscn files)
- Reusable blueprints
- Can be instanced multiple times

### Project Organization
- Separate folders for scenes, scripts, and assets
- Use descriptive file names (snake_case)
- Always move files within Godot's FileSystem panel

## 🎓 Week 1 Progress

- [x] Project setup & folder structure
- [x] Understanding nodes & scenes
- [x] Created first scene (Node2D with Sprite)
- [x] Basic automatic movement
- [ ] User input (arrow keys)
- [ ] Player movement scene
- [ ] Enemy scene practice

## 🔗 Resources

- [Official Godot Docs](https://docs.godotengine.org/)
- [GDScript Basics](https://docs.godotengine.org/en/stable/tutorials/scripting/gdscript/gdscript_basics.html)

## ✍️ Author

Monalisa Sabina - Learning game development with Godot

---

**Current Status:** Week 1 - Learning nodes & scenes fundamentals  
**Last Updated:** [Current Date]