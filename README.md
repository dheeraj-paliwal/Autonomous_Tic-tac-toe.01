# Autonomous_Tic-tac-toe.01
# Java Tic-Tac-Toe with Random Computer Opponent

This is a simple Java implementation of the classic Tic-Tac-Toe game, featuring a random computer opponent.

## Features

* **Interactive Gameplay:** Play Tic-Tac-Toe in the console.
* **Random Computer Opponent:** The computer makes random moves, providing a basic challenge.
* **Random Turn Selection:** The game randomly decides who starts (player or computer).
* **Input Validation:** Ensures the user enters valid input and selects available squares.
* **Win/Draw Detection:** Accurately detects win and draw conditions.

## How to Run

1.  **Clone the Repository:**
    ```bash
    git clone [repository URL]
    cd [repository directory]
    ```
2.  **Compile the Java Code:**
    ```bash
    javac com/mcnz/tictactoe/Main.java
    ```
3.  **Run the Game:**
    ```bash
    java com.mcnz.tictactoe.Main
    ```

## Code Explanation

* **`Main.java`:**
    * Contains the main game logic.
    * Uses a `char[]` array to represent the Tic-Tac-Toe board.
    * Handles player input and computer moves.
    * Implements methods to print the board, check for win/draw conditions, and manage game flow.
* **`computerMove()`:**
    * Generates random moves for the computer player.
    * Ensures the computer selects an available square.
* **`getTheUserToSelectTheirSquare()`:**
    * Handles user input and validates it.
* **`theyWonTheGame()`:**
    * Checks all possible winning combinations.
* **`printTheBoard()`:**
    * prints the current state of the board.

## Improvements and Future Work

* Implement a smarter AI for the computer opponent (e.g., using minimax algorithm).
* Add a graphical user interface (GUI).
* Allow players to choose their markers (X or O).
* Add a play again function.

## Contributing

Feel free to contribute to this project by submitting pull requests or opening issues for bug reports or feature requests.

## License

This project is open-source. Feel free to use and modify it as you wish.

