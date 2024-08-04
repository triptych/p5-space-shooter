# Space Shooter Game

This is a simple space shooter game built with p5.js. The game features a player-controlled ship, randomly generated enemies, and a scrolling starfield background.

## Game Structure

The game is built using object-oriented programming principles in JavaScript. Here's an overview of the main components:

### Global Variables

- `ship`: The player's ship object.
- `bullets`: An array of bullet objects fired by the player.
- `enemies`: An array of enemy objects.
- `stars`: An array of star objects for the background.
- `particles`: An array of particle objects for explosion effects.
- `score`: The player's current score.
- `gameOver`: A boolean flag indicating whether the game has ended.

### Setup Function

The `setup()` function is called once at the beginning of the game. It:
- Creates the canvas using the window's dimensions.
- Initializes the player's ship.
- Populates the `stars` array for the background.

### Draw Function

The `draw()` function is the main game loop, called continuously. It:
- Updates and displays the starfield background.
- If the game is not over:
  - Displays the player's ship.
  - Updates and displays bullets.
  - Generates new enemies randomly.
  - Updates and displays enemies.
  - Checks for collisions between bullets and enemies, and between the ship and enemies.
  - Handles mobile controls.
- Updates and displays particle effects.
- Displays the current score.
- Shows the game over screen if the game has ended.

### Classes

1. `Ship`: Represents the player's ship. It can move and detect collisions.
2. `Bullet`: Represents bullets fired by the player. They move upward and can be checked for collisions.
3. `BlockyEnemy`: Represents enemies. They move downward, can be hit by bullets, and can collide with the player.
4. `Star`: Represents background stars. They move downward to create a scrolling effect.
5. `Particle`: Used for explosion effects when enemies are destroyed or the player's ship is hit.

### Helper Functions

- `createExplosion(x, y)`: Creates particle effects at the given coordinates.
- `restartGame()`: Resets the game state for a new game.
- `createBlockyEnemy(x, y)`: Generates a new enemy with a random blocky shape.

### Input Handling

- `keyPressed()`: Handles keyboard input for shooting and restarting the game.
- `touchStarted()`: Handles touch input for shooting and restarting the game on mobile devices.
- `mouseMoved()`: Updates the ship's position based on mouse movement.
- `touchMoved()`: Updates the ship's position based on touch movement on mobile devices.

## Game Mechanics

1. The player controls a ship at the bottom of the screen, which can move horizontally and vertically in the lower half of the screen.
2. Enemies spawn randomly from the top of the screen and move downward.
3. The player can shoot bullets to destroy enemies.
4. If an enemy collides with the player's ship, the game ends.
5. The player scores points for each enemy destroyed.
6. The game features a scrolling starfield background for a sense of movement.
7. Particle effects are used to create explosions when enemies are destroyed or when the player's ship is hit.

## How to Run

1. Ensure you have the p5.js library linked in your HTML file.
2. Copy the entire JavaScript code into a `<script>` tag in your HTML file.
3. Open the HTML file in a web browser.

## Controls

- On desktop:
  - Move the mouse to control the ship's position.
  - Press the spacebar to shoot.
- On mobile:
  - Touch and drag to move the ship.
  - Tap the screen to shoot.
- After game over, press any key or tap the screen to restart.

Feel free to modify and extend this game as you see fit!