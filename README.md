# Civ-Style Game (prototype)

A small Unity prototype inspired by Civilization-style strategy games.

This project experiments with a hex-based world, procedural terrain generation, selectable units, settlement placement, basic resources, UI panels, and simple pathfinding/AI systems.

> This is an older experimental project, not a fully functioning game.

## Features

- Procedurally generated hex-based terrain
- Multiple terrain types
  - Deep water
  - Shallow water
  - Grass
  - Forest
  - Mountains
- Selectable units
- Unit movement and path previews
- Settler units that can found settlements
- Basic resource tracking
  - Gold
  - Iron
  - Wood
  - Stone
- Entity information UI
- Basic crafting/menu UI
- Camera movement and zoom controls
- A* pathfinding
- Simple enemy AI logic
- Unit health, movement, attack range, and damage systems

## Terrain Generation

The world is generated using Perlin noise to create a height map.

Different height ranges are used to determine which type of hex tile is placed:

```text
Lower values  -> Deep Water
               -> Shallow Water
               -> Grass
               -> Forest
Higher values -> Mountains
```

The default map size in the current project is `200 x 200` tiles.

## Units

Units can be selected and moved around the world.

The settler unit supports:

- Left-click selection
- Right-click movement
- Path previews
- Settlement placement
- Hex-grid snapping when founding a settlement

The project also contains a more general unit system with:

- Health
- Strength
- Movement speed
- Attack range
- Damage variation
- Turn states
- Movement
- Attacking
- Death

## Pathfinding and AI

The project contains an A* pathfinding implementation for movement across the hex grid.

There is also a basic AI system that:

1. Chooses one of its available units
2. Finds an enemy target
3. Moves toward that target
4. Attacks when in range

The AI is fairly simple and was mainly made as an experiment with turn-based strategy behavior.

## Controls

### Camera

```text
W / Arrow Up       Move camera forward
S / Arrow Down     Move camera backward
A / Arrow Left     Move camera left
D / Arrow Right    Move camera right
Mouse Wheel        Zoom
Middle Mouse       Drag/pan camera
```

### Units

```text
Left Click         Select a unit or entity
Right Click        Move selected unit / deselect entity
```

Settler units also expose a settlement button when selected.

## UI

The project includes UI systems for:

- Resource counts
- Selected entity information
- Health
- Movement speed
- Menus
- Crafting panels

## Opening the Project

This project was made with:

```text
Unity 2021.3.19f1
```

To open it:

1. Install Unity Hub.
2. Install Unity `2021.3.19f1`, or a compatible Unity version.
3. Clone or download this repository.
4. Add the project through Unity Hub.
5. Open the project.

Unity may need some time to import and rebuild the project files the first time it opens.

## Project Structure

```text
Assets/
├── AllAssets/
│   ├── Docs/
│   └── Scripts/
│       ├── AI.cs
│       ├── AStar.cs
│       ├── HexGrid.cs
│       ├── HexPosition.cs
│       └── Unit.cs
│
└── scripts/
    ├── Game/
    │   ├── Controlls/
    │   ├── UI/
    │   ├── Units/
    │   └── World/
    │
    └── Utils/
```

Some of the systems in `AllAssets` are separate or earlier implementations used while experimenting with the hex-grid and unit systems.

## Status

This is a prototype rather than a finished Civilization-style game.

A number of systems are incomplete or experimental, but the repository contains the foundations for:

- procedural world generation
- strategy-game camera controls
- units
- settlements
- resources
- pathfinding
- combat
- basic AI

## License

See the license included in the repository for usage and redistribution terms.
