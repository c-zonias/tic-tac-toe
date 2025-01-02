# Tic-Tac-Toe Game

This project is a simple implementation of the classic Tic-Tac-Toe game in Python. It is designed for two players, with each taking turns to play as either `X` or `O`. The game is interactive and text-based, making it easy to play directly in the terminal.

## How to Play

1. **Objective**: The goal of the game is to align three of your marks (`X` or `O`) either horizontally, vertically, or diagonally on a 3x3 grid before your opponent does.
2. **Inputs**: Players input a number between 1 and 9 to place their mark in the corresponding cell of the grid. The grid cells are numbered as follows:
   ```
   1 | 2 | 3
   ---------
   4 | 5 | 6
   ---------
   7 | 8 | 9
   ```
3. **Rules**:
   - A cell can only be marked if it is empty (`-`).
   - If a player inputs an invalid number or selects an already marked cell, they will be prompted to try again.

## Features

- **Interactive Gameplay**: The game prompts each player with their turn and highlights errors if any invalid moves are made.
- **Dynamic Board**: The grid updates in real-time after each move.
- **Winner Detection**: The game checks for a winner after each turn and announces the result immediately.
- **Tie Detection**: If all cells are filled and no winner is determined, the game declares a tie.

## Code Overview

### Global Variables
- `board`: Represents the 3x3 game grid.
- `currentPlayer`: Tracks the player whose turn it is (`X` or `O`).
- `winner`: Stores the winner of the game (if any).
- `gameRunning`: A flag to keep the game running until it ends.

### Functions

1. **`printBoard(board)`**
   Displays the current state of the board in a visually appealing format.

2. **`playerInput(board)`**
   Prompts the current player to input a move, validates the input, and updates the board accordingly.

3. **`checkHorizontal(board)`**
   Checks for a winning condition in the horizontal rows.

4. **`checkRow(board)`**
   Checks for a winning condition in the vertical columns.

5. **`checkDiagonal(board)`**
   Checks for a winning condition in the diagonal lines.

6. **`checkTie(board)`**
   Checks if the board is full and declares a tie if no winner is found.

7. **`checkWin()`**
   Combines all winning checks and announces the winner if any.

8. **`switchPlayer()`**
   Alternates the `currentPlayer` between `X` and `O`.

### Game Loop
The game runs in a loop, displaying the board, accepting inputs, checking for a winner or tie, and switching players until the game concludes.

## Example Gameplay
```plaintext
- | - | -
---------
- | - | -
---------
- | - | -
Enter a number 1-9 Player (X) : 1
X | - | -
---------
- | - | -
---------
- | - | -
Enter a number 1-9 Player (O) : 5
X | - | -
---------
- | O | -
---------
- | - | -
...
The winner is X
```

## How to Run
1. Install Python (if not already installed).
2. Copy the code into a `.py` file.
3. Open a terminal and run the script using:
   ```bash
   python <filename>.py
   ```
4. Follow the prompts to play.

## Future Enhancements
- Add a graphical user interface (GUI).
- Implement an AI opponent for single-player mode.
- Allow customizable board sizes.

Enjoy playing Tic-Tac-Toe!

