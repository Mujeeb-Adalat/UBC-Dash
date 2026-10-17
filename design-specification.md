# UBC-Dash Design Specification

## Problem

UBC students often have short periods of free time between classes, labs and other academic commitments, but these breaks are not always long enough for more involved activities. At the same time, university life can be stressful, and students benefit from quick, low-commitment ways to relax and engage with others.
UBC also has a strong culture built around shared experiences, faculty stereotypes, course-related jokes, and friendly competition between students. However, there are relatively few lightweight UBC-specific interactive experiences that combine these aspects of campus culture in a way that students can enjoy during short breaks.

## Solution

UBC-Dash is a 2D platformer game inspired by UBC campus life. The player controls a character though a sequence of increasingly difficult stages themed around UBC buildings, faculties, courses, and student experiences.
The player must navigate platforms, void obstacles and hazards, and reach the end of each stage. As the player progresses, stages introduce new obstacle types, faster movement, tighter timing, and more difficult platforming challenges.
The player receives a score based on their performance. At the end of a run, the player may submit their score to an online leaderboard and compare their results with other players.

### Main Menu

When the application starts, the player is shown a main menu with the game title and the following options:
- Start Game
- View Leaderboard
- Exit

Selecting Start Game begins a new run from the first stage.
Selecting View Leaderboard opens the online leaderboard, where the player can view the highest submitted scores.
Selecting Exit closes the application.

#### Main Menu Mockup

<img width="326" height="173" alt="image" src="https://github.com/user-attachments/assets/457676fa-e967-4bf8-b06d-c2229005c6c4" />


### Gameplay

The player controls a character in a 2D side-scrolling platform environment. The player can move left, move right, and jump. The goal of each stage is to reach the end while avoiding hazards and navigating platforms. The player begins each run with three lives. The number of remaining lives is displayed during gameplay. If the player collides with a hazard, the player loses one life and the current stage restarts from the beginning. If the player loses all three lives, the run ends and the Game Over screen is shown. The player must then start a new run from the first stage. Each stage becomes more difficult than the previous one by introducing new obstacles, faster-moving hazards, more precise jumps, or combinations of previously introduced mechanics. When the player successfully reaches the end of a stage, the next stage begins.

### Scoring

The player earns points based on the number of stages completed, the total time taken, and the number of lives lost during the run. Each completed stage adds **1000 points** to the player's score. Time acts as a score penalty. For every second that passes during the run, **5 points** are deducted from the player's score. Each time the player loses a life, an additional **250 points** are deducted.

The player's score is calculated as:

**Score = (1000 × stages completed) - (5 × total seconds elapsed) - (250 × lives lost)**

The player's score cannot fall below 0. Restarting a stage does not reset the total elapsed time or remove any score penalties already accumulated during the run. The current score is displayed during gameplay. When the run ends, either by completing all stages or by losing all three lives, the player's final score is displayed.

#### Score Summary Mockup

<img width="287" height="121" alt="image" src="https://github.com/user-attachments/assets/7a7e1a0b-0820-4f48-bf73-3a17b18bf4e8" />


### Leaderboard

The player can view the online leaderboard from the Main Menu. The leaderboard displays the highest submitted scores from all players. Each leaderboard entry shows the player's name and final score, with entries ordered from highest score to lowest score. At the end of a run, the player is given the option to enter a name and submit their final score to the leaderboard. If the player does not want to submit the score, they may skip submission and return to the Main Menu. If the leaderboard server cannot be reached, the game displays an error message informing the player that the online leaderboard is temporarily unavailable. The player can still return to the Main Menu and continue playing the game normally.

#### Leaderboard Mockup

<img width="257" height="155" alt="image" src="https://github.com/user-attachments/assets/84a4f8eb-1902-41bd-a54d-82e81395dd8b" />


### Game Over and Run Complete

A run ends when either the player loses all three lives or successfully completes the final stage. If the player loses all three lives, a Game Over screen is shown. This screen displays the message "Game Over" and prompts the player to press any key to continue. If the player completes the final stage, a Run Complete screen is shown. This screen displays the message "Run Complete" and indicates that all stages have been completed successfully. The player is then prompted to press any key to continue. After the player presses a key on either screen, a score summary screen is shown. This screen displays the player's run statistics, final score, and the option to submit the score to the online leaderboard. After submitting or skipping score submission, the player is returned to the Main Menu.

#### 1. Game Over Mockup

<img width="322" height="121" alt="Game Over" src="https://github.com/user-attachments/assets/639fc5ac-f3c8-4e57-96c0-a224062a4ee0" />

#### 2. Run Complete Mockup

<img width="323" height="143" alt="Run Complete" src="https://github.com/user-attachments/assets/98c94286-a73a-4276-a9eb-d2ba5f058cf6" />

### Controls

The player controls the character using the keyboard.

- **A** or **Left Arrow**: Move left
- **D** or **Right Arrow**: Move right
- **W** or **Up Arrow**: Jump
- **Escape**: Pause the game

The player may use either the arrow keys or the equivalent WASD controls during gameplay. Mouse input may be used to select buttons in menus such as Start Game, View Leaderboard, Submit Score, and Exit.

### Pause Menu

Pressing Escape during gameplay pauses the game. While the game is paused, player movement, hazards, timers, and other gameplay activity stop.

The Pause Menu provides the following options:

- Resume Game
- Restart Stage
- Return to Main Menu

Selecting Resume Game continues the current stage from the point where it was paused. Selecting Restart Stage restarts the current stage from the beginning. Restarting a stage does not reset the player's total elapsed time, current score, lives lost, or any score penalties already incurred during the run. Selecting Return to Main Menu ends the current run and returns the player to the Main Menu.

#### Pause Menu Mockup

<img width="323" height="169" alt="image" src="https://github.com/user-attachments/assets/6588547c-e540-4d93-98e6-1eb25ee742b9" />

