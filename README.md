# 🎮 Java 2D Platformer

A hand-crafted 2D side-scrolling platformer built in pure Java using the AWT/Swing rendering pipeline — no game engine, no external libraries.

---

## Features

- Smooth player movement with physics — running, jumping, falling
- Three enemy types: **Crabby**, **Pinkstar**, and **Shark**, each with unique AI and attack patterns
- Five handcrafted levels with tile-based collision
- Collectable potions, destructible containers, spike traps, and cannons
- Animated rain particle effects and scrolling parallax backgrounds
- Full audio system — background music per level, SFX for attacks, jumps, and death
- Pause menu with volume and sound toggle controls
- Game over, level completed, and game completed screens
- Scrolling credits screen

---

## Getting Started

### Prerequisites

- **Java 21** or higher ([Download](https://adoptium.net/))
- No build tool required — plain `javac` is enough

### Build

```bash
javac --release 21 -d bin -sourcepath src $(find src -name "*.java")
```

> **Windows (PowerShell)**
> ```powershell
> Get-ChildItem -Recurse -Filter "*.java" src |
>   Select-Object -ExpandProperty FullName |
>   Out-File sources.txt
> javac --release 21 -d bin -sourcepath src -cp bin (Get-Content sources.txt)
> ```

### Run

```bash
java -cp bin main.MainClass
```

---

## Controls

| Key | Action |
|---|---|
| `A` / `D` or `←` / `→` | Move left / right |
| `Space` or `W` or `↑` | Jump |
| `F` | Attack |
| `Esc` | Pause / back to menu |

---

## Project Structure

```
PlatformerTutorial/
├── src/
│   ├── audio/          # AudioPlayer — music & SFX
│   ├── effects/        # Rain particles, dialogue effects
│   ├── entities/       # Player, Enemy base, Crabby, Pinkstar, Shark
│   ├── gamestates/     # Menu, Playing, Credits, GameOptions, state machine
│   ├── inputs/         # Keyboard & mouse input handlers
│   ├── levels/         # Level loading & management
│   ├── main/           # Game loop, window, panel
│   ├── objects/        # Potions, containers, cannons, spikes, trees
│   ├── ui/             # HUD, pause overlay, buttons, audio controls
│   └── utilz/          # Constants, LoadSave, HelpMethods
├── res/                # All game assets (sprites, audio, level maps)
│   ├── audio/
│   └── lvls/
└── bin/                # Compiled output (git-ignored)
```

---

## Team

| | Name | Role | ID |
|---|---|---|---|
| | Radoan Moktaken Jaman | Lead Developer | 4085 |
| | Abrar Ahomed | Developer | 3159 |
| | Tasnim Islam | Developer | 4138 |

---

## License

This project is for educational purposes.
