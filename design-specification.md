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

### Gameplay

The player controls a character in a 2D side-scrolling platform environment.
The player can move left, move right, and jump. The goal of each stage is to reach the end while avoiding hazards and navigating platforms.
Each stage becomes more difficult than the previous one by introducing new obstacles, faster-moving hazards, more precise jumps, or combinations of previously introduced mechanics.
If the player collides with a hazard, the player either loses a life or restarts the current stage. The exact penalty will be finalized during implementation.
When the player reaches the end of a stage, the next stage begins.

### Scoring

The player earns a score based on their performance during the run.

The score may take into account factors such as:

- stages completed;
- time taken;
- obstacles cleared;
- deaths or retries.

The final scoring formula will be finalized before implementation.

At the end of a run, the player's final score is displayed.
