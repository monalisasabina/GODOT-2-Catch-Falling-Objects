# Scenes

## Simple Definition:
A **scene** is a **saved collection of nodes** organized in a tree.

**Scene = Nodes + Structure saved as a file**

### Analogy:
- **Nodes** = LEGO bricks
- **Scene** = A completed LEGO model (saved so you can rebuild it)

---


## Part 2: Scene Example - Building a Coin

Let's build a collectible coin step by step.

### Step 1: Create the Node Tree
```
Area2D (detects when player touches it)
├── Sprite2D (shows coin image)
└── CollisionShape2D (defines coin's touchable area)
```

### Step 2: Save as a Scene
- File → Save Scene
- Name it: `coin.tscn`
- Location: `scenes/coin.tscn`

**Now you have a reusable coin scene!**

---

## Part 3: Using Scenes (Instancing)

**Once you save a scene, you can use it multiple times.**

### Create a Level Scene:
```
Node2D (main level)
├── Coin1 (instance of coin.tscn)
├── Coin2 (instance of coin.tscn)
├── Coin3 (instance of coin.tscn)
└── Background (Sprite2D)
```

Place Coins in Your Level (Do This Multiple Times):

1. Open main.tscn (your level)
2. Right-click the root node → "Instantiate Child Scene"
3. Select coin.tscn
4. A coin appears in your level!
5. Drag it to position it where you want
6. Repeat steps 2-5 to add more coins at different positions

**You created ONE coin scene, but placed it 3 times in your level!**

### This is Like:
- **Scene** = Cookie cutter
- **Instance** = Actual cookies made from the cutter
- You can make 100 cookies from one cutter

---

## Part 4: Real Example - Building a Simple Player from earlier

### What We Need:
- A way to move (CharacterBody2D)
- A visual image (Sprite2D)
- A way to detect collisions (CollisionShape2D)

###  Create the root node:
- Click the "+" tab (next to your current scene tab) OR go to Scene → New Scene
- Click "Other Node" in "Create Root Node"
- Search for "CharacterBody2D"
- Click "Create"

### Add child nodes:
- Right-click CharacterBody2D → "Add Child Node"
- Search for "Sprite2D" → "Create"
- Right-click CharacterBody2D → "Add Child Node"
- Search for "CollisionShape2D" → "Create"

###  Add an image to Sprite2D:
- Click Sprite2D in the tree
- Look at Inspector (right panel)
- Find "Texture" property
- Click dropdown → "Load"
- Select icon.svg from your assets
- You'll see the Godot icon appear!

###  Change the sprite color (to look like a player):
- Keep Sprite2D selected
- In Inspector, find "Modulate" property (under visibility)
- Click the color box
- Change to a different color (like blue, green, or red)
- This differentiates your player from other objects

### Make it smaller (optional):
- Keep Sprite2D selected
- In Inspector → Transform → Scale
- Set both X and Y to 0.5 (or whatever size you want)

### Set up the collision shape:
- Click CollisionShape2D
- In Inspector, find "Shape" property
- Click dropdown → "New RectangleShape2D"
- Click the shape again to edit size
- In the viewport, drag the orange handles to match your sprite size

### Save the scene:
- Press Ctrl+S
- Name: player_character.tscn
- Location: Scenes/characters/
- Click "Save"

### Player structure
```
CharacterBody2D (handles movement/physics)
├── Sprite2D (visual appearance)
└── CollisionShape2D (collision detection)
```

## Part 5: Understanding Scene Files (.tscn)
- When you save a scene, Godot creates a .tscn file. 

- It's a text file that describes your scene structure.

- Example: What's inside player.tscn?
```
[node name="CharacterBody2D" type="CharacterBody2D"]

[node name="Sprite2D" type="Sprite2D" parent="."]
texture = ExtResource("1_abc123")
modulate = Color(0, 0.5, 1, 1)

[node name="CollisionShape2D" type="CollisionShape2D" parent="."]
shape = SubResource("RectangleShape2D_xyz789")
```

It describes:
1. What nodes exist (CharacterBody2D, Sprite2D, CollisionShape2D)
2. How they're organized (parent/child relationships)
3. What properties they have (texture, color, shape)
4. What resources they use (images, shapes, etc.)
