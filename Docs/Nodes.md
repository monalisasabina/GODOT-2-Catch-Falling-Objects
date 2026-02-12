# Nodes 

## Node
### 1. Definition
- is a single building block in Godot... like  a LEGO brick

- each node has a specific job:
1. Sprite2D - Shows an image on screen
2. AudioStreamPlayer - Plays a sound
3. Timer - Counts down time
4. Camera2D - Controls what the player sees
5. Label - Displays text
6. CollisionShape2D - Detects when things bump into each other
7. CharacterBody2D - Handles player/enemy movement with physics

- one node = one job

### 2. nodes are like HTML elements

```html
<div>
  <img src="player.png">
  <p>Health: 100</p>
</div>
```

```
Node2D (like <div>)
├── Sprite2D (like <img>)
└── Label (like <p>)
```

**Each element/node does one thing, and you combine them to create something bigger.**

### Part 3: The Node Tree (Hierarchy)

Nodes are organized in a **tree structure** with parents and children:
```
Parent Node
├── Child Node 1
├── Child Node 2
└── Child Node 3
    └── Grandchild Node
```

#### Example - A Simple Player:
```
CharacterBody2D (Parent - handles movement/physics)
├── Sprite2D (Child - shows player image)
├── CollisionShape2D (Child - detects hits)
└── Camera2D (Child - follows player)
```

**The parent is the "container" that holds all the child nodes.**

---

### Part 4: Why Use Parent-Child Relationships?

#### When the Parent Moves, Children Move Too!

**Example:**
```
Player (at position 100, 100)
├── Sprite (at position 0, 0 relative to parent)
└── Weapon (at position 20, 0 relative to parent)
```

**If you move the Player to (200, 200):**
- Sprite automatically moves to (200, 200)
- Weapon automatically moves to (220, 200)
- They stay attached!

**It's like:**
- Parent = your body
- Children = your arms, legs, head
- When your body moves, everything moves with it

---