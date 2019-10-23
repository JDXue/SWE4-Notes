# 24 Oct
## Personal Project Week 1: Connect4

(sourced from CodeWars)
### Task

The game consists of a grid (7 columns and 6 rows) and two players that take turns to drop their discs. The pieces fall straight down, occupying the next available space within the column. The objective of the game is to be the first to form a horizontal, vertical, or diagonal line of four of one's own discs.

Your task is to create a Class called Connect4 that has a method called play which takes one argument for the column where the player is going to place their disc.

### Rules

* If a player successfully has 4 discs horizontally, vertically or diagonally then you should return "Player n wins!” where n is the current player either 1 or 2.

    * There must be two players that can play against one another

* If a player attempts to place a disc in a column that is full then you should return ”Column full!” and the next move must be taken by the same player.

* If the game has been won by a player, any following moves should return ”Game has finished!”.

* Any other move should return ”Player n has a turn” where n is the current player either 1 or 2.

* Player 1 starts the game every time and alternates with player 2.

* The columns are numbered 0-6 left to right.



### Project Tasks
Steps for versions created using MVP making test-based goals

* | O O O
* | O O O
* | O O O


#### Version 1 - Noughts and Crosses 3 x 3 version
* Setup
    * Make new game instance
    * Display 2D array with no moves
    * Define Player 1 and 2 - assign counter color

* Allow player 1 to enter counter based on column number
    * Get player 1 input
    * Check if column is available
    * Display player's counter in array

* Check player 2 can also enter counters identifiable from player 1
    * Display player 2's counter in array

* Validation of Win / Endgame
    * After both players have had 4 goes, check if either have won
        * Check horizontal
        * Check vertical
        * Check diagonals

    * Given that a player has got four in a row, display message with winning player
    * Given that the board is full, and no person has got a row of four


