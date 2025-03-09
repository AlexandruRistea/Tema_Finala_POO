# Enemy Battle Game

This is a simple game where different types of enemies interact with the player. The game uses object-oriented principles such as inheritance, polymorphism, the singleton pattern, and factory methods to manage enemy creation and game state.

## Features

- **Enemy Classes**: The base `Inamic` class has three derived classes:
  - `Mic` (small enemy)
  - `Mediu` (medium enemy)
  - `Mare` (large enemy)
- **Attributes**: Each enemy has:
  - `viata` (health)
  - `atac` (attack power)
- **Methods**:
  - `getAtac()`: Returns the attack power.
  - `getViata()`: Returns the current health.
  - `takeDmg(int dmg)`: Reduces health when attacked.
- **Error Handling**:
  - `eroareViata`: Raised when an enemy with 0 health is attacked.
  - `eroareAtac`: Raised when an attack is not initialized.
- **Game Manager**: Ensures that all game modifications go through a single instance using the Singleton pattern.
- **Factory Pattern**: Enemies are created using a factory method.
- **Templates**:
  - `mecanici`: Checks values like HP/attack between two characters.
  - `Date`: Stores player attributes such as map coordinates and movement speed.

## How It Works

1. The game starts and initializes enemies using the Factory Pattern.
2. The `Manager` ensures all operations follow a controlled flow.
3. Each enemy can speak (`vorbeste()`), attack, and take damage.
4. If an enemy’s attack or health is invalid, an exception is thrown.

## Installation & Usage

1. Compile the program:
   ```sh
   g++ -o game main.cpp joc.cpp mare.cpp mediu.cpp mic.cpp Inamic.cpp -std=c++11
   ```
2. Run the game:
   ```sh
   ./game
   ```

## Future Improvements

- Add player interaction and combat mechanics.
- Implement AI for enemy movement and behavior.
- Introduce a graphical interface.

