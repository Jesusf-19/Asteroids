# Asteroids

Asteroids is a Python/Pygame arcade-style game inspired by the classic Asteroids game. The player controls a triangular spaceship, moves around the screen, shoots projectiles, avoids incoming asteroids, and destroys asteroids by shooting them.

## Description

This project was built using Python and Pygame. It focuses on object-oriented programming concepts such as classes, inheritance, method overriding, sprite groups, collision detection, and game loop updates.

The game includes:

* A player-controlled spaceship
* Player movement using `W`, `A`, `S`, and `D`
* Shooting with the spacebar
* Shot cooldown timing
* Asteroids that spawn from the edges of the screen
* Collision detection between the player, shots, and asteroids
* Asteroid splitting when larger asteroids are destroyed
* Game over when the player collides with an asteroid
* Basic game event logging

## Controls

| Key        | Action        |
| ---------- | ------------- |
| `W`        | Move forward  |
| `S`        | Move backward |
| `A`        | Rotate left   |
| `D`        | Rotate right  |
| `Spacebar` | Shoot         |

## Project Structure

```text
Asteroids/
├── asteroid.py
├── asteroidfield.py
├── circleshape.py
├── constants.py
├── game_events.jsonl
├── logger.py
├── main.py
├── player.py
├── shot.py
├── pyproject.toml
├── uv.lock
├── .python-version
├── .gitignore
└── README.md
```

## Main Files

### `main.py`

The main entry point of the game. It initializes Pygame, creates sprite groups, creates the player and asteroid field, runs the game loop, updates objects, checks collisions, draws objects, and handles quitting the game.

### `player.py`

Contains the `Player` class. The player inherits from `CircleShape`, uses a circular hitbox, and is drawn as a triangle. The player can rotate, move forward and backward, and shoot projectiles with a cooldown timer.

### `shot.py`

Contains the `Shot` class. Shots inherit from `CircleShape`, move using a velocity vector, and are drawn as small circles.

### `asteroid.py`

Contains the `Asteroid` class. Asteroids move across the screen, can collide with the player or shots, and can split into smaller asteroids when destroyed.

### `asteroidfield.py`

Handles asteroid spawning. Asteroids are created from random screen edges with random sizes, speeds, and movement directions. (File provided)

### `circleshape.py`

Base class for circular game objects. It stores position, velocity, radius, and includes shared collision detection logic using the distance between two circular objects.

### `constants.py`

Stores important game settings such as screen size, player speed, player radius, asteroid sizes, shot speed, and cooldown values.

### `logger.py`

Handles game state and event logging. (File provided)

## Features

* Object-oriented game structure
* Pygame sprite groups for update and draw management
* Vector-based movement using `pygame.Vector2`
* Circular collision detection
* Player shooting system
* Shot cooldown system
* Asteroid spawning system
* Asteroid splitting behavior
* Game over detection
* Event logging for gameplay actions

## Requirements

This project uses:

* Python 3.13 or higher
* Pygame 2.6.1
* uv for project/package management

## How to Run

Clone the repository:

```bash
git clone https://github.com/Jesusf-19/Asteroids.git
```

Move into the project folder:

```bash
cd Asteroids
```

Run the game with uv:

```bash
uv run main.py
```

If you are not using uv, install Pygame manually:

```bash
pip install pygame==2.6.1
```

Then run:

```bash
python3 main.py
```

## Gameplay

When the game starts, the player spawns in the middle of the screen. Asteroids spawn from the edges and move across the screen. The player must avoid the asteroids while shooting them.

If a shot hits an asteroid, the asteroid is destroyed. Larger asteroids split into smaller asteroids. If the player collides with an asteroid, the game prints a game over message and exits.

## Concepts Practiced

This project helped practice:

* Python classes
* Inheritance
* Method overriding
* Pygame basics
* Sprite groups
* Game loops
* Delta time movement
* Vector math
* Collision detection
* Object spawning
* Project organization

## Future Improvements

Possible future improvements include:

* Add a score system
* Add lives or health
* Add screen wraparound for the player
* Add sound effects
* Add a start menu
* Add a restart option after game over
* Add different asteroid colors or sizes
* Add explosion effects
* Add a high score tracker

## Author

Jesus Fierro
