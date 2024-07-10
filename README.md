# BreakoutAI

## Project Overview

This project implements an AI agent to play the classic Atari Breakout game. The agent is trained using Q-learning and Approximate Q-learning algorithms. Our approach involves multiple stages of state compression, feature extraction, and performance optimization to achieve an effective game-playing agent.

## Game Description

In Breakout, the objective is to break all the bricks at the top of the screen using a ball. The player controls a paddle to prevent the ball from falling. The game ends when the player loses all five balls or breaks all the bricks.

## Action Space
- `2`: Paddle moves right
- `3`: Paddle moves left
- `0`: Paddle remains stable

## Observation Space
- Dimensions: 210 x 160 x 3

## Stages of Development

### Stage 1: Random Actions
Initially, the paddle performed actions randomly. This resulted in poor performance.

### Stage 2: Q-learning
We attempted to train the agent using Q-learning, but the large state space made this approach impractical. We reduced the state space by converting images to grayscale and resizing them to 84 x 84.

### Stage 3: State Feature Extraction
We extracted specific features such as the angle and distance of the ball from the paddle, which significantly improved the agent's performance.

### Stage 4: Approximate Q-learning
We used approximate Q-learning due to the inefficacy of standard Q-learning for this game. This method involves using features to represent states and adjusting weights based on experience.

### Stage 5: Optimized Approximate Q-learning
We optimized the agent by considering additional features like the direction and speed of the ball. This improved the agent's speed and ability to make better decisions.

## Features

### Image Processing
- **Ball and Paddle Detection**: Using RGB values to identify the ball and paddle positions.
- **Feature Extraction**: Calculating distances and counting unbroken bricks.

### Performance Improvements
- **Speed Optimization**: Ignoring non-relevant states where the ball is not near the paddle.
- **Feature Enhancement**: Including ball trajectory predictions.

## Results
- The agent's performance improved significantly through each stage.
- The final implementation demonstrates a high level of skill in playing Breakout, avoiding losses, and achieving high scores.


### Demonstration Videos
- **Approximate Q-learning Result**: [ApproximateQLearning.mp4](videos/ApproximateQLearning.mp4)
- **Best Performance**: [Final.mp4](videos/Final.mp4)
