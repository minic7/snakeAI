# Snake Game AI with Pygame

This repository contains an AI-controlled implementation of the classic Snake game using Pygame. The AI navigates the game board to eat food and grow in length, making decisions based on an action array.

## Features

- **AI-controlled Snake**: The snake's movements are controlled by an AI that interprets action arrays.
- **Pygame-based game engine**: Utilizes the Pygame library for graphics and event handling.
- **Dynamic game state**: Real-time updates of the game state, including the snake's position, direction, and score.

## Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/yourusername/snake-game-ai.git
   cd snake-game-ai
   ```

2. **Install dependencies**:
   Ensure you have Python and Pygame installed. You can install Pygame and Numpy using pip:
   ```sh
   pip install pygame numpy
   ```

3. **Run the game**:
   ```sh
   python snake_game.py
   ```

## Game Mechanics

### AI Controls

The AI's actions are determined by an action array `[straight, right, left]`. The AI can decide to move straight, turn right, or turn left based on this array.

### Scoring

- **Eating food**: +10 points.
- **Collisions**: -10 points, ends the game.
- **Time-based penalty**: The game ends if the snake does not eat food within a certain number of frames proportional to its length.

### Game Over Conditions

- Collision with the game boundary.
- Collision with itself.
- Surpassing a time limit without eating food.

## Code Overview

### Main Components

- **Direction Enum**: Defines possible movement directions for the snake.
- **Point NamedTuple**: Represents points on the game board.
- **SnakeGameAI Class**: Encapsulates the game logic, including initialization, game state updates, rendering, and collision detection.

### Key Methods

- **`__init__(self, w=640, h=480)`**: Initializes the game with a specified width and height.
- **`reset(self)`**: Resets the game state to start a new game.
- **`_place_food(self)`**: Randomly places food on the game board, ensuring it does not overlap with the snake.
- **`play_step(self, action)`**: Executes a game step based on the AI's action.
- **`is_collision(self, pt=None)`**: Checks for collisions with boundaries or the snake itself.
- **`_update_ui(self)`**: Renders the game board and snake on the screen.
- **`_move(self, action)`**: Updates the snake's direction and position based on the action array.

## Customization

You can customize various aspects of the game, including:
- **Block size**: Adjust the size of the snake and food blocks by changing the `BLOCK_SIZE` constant.
- **Game speed**: Modify the `SPEED` constant to control how fast the game runs.
- **Window size**: Change the width (`w`) and height (`h`) parameters when initializing `SnakeGameAI`.

## Future Improvements

- **Enhanced AI**: Implement advanced algorithms for better decision-making.
- **Difficulty levels**: Introduce different difficulty levels by adjusting game speed and AI behavior.
- **User-controlled Snake**: Allow users to control the snake with keyboard inputs.

## Contributing

Feel free to fork this repository, make improvements, and submit pull requests. Contributions are welcome!



---

Enjoy the game! If you have any questions or feedback, please don't hesitate to reach out.