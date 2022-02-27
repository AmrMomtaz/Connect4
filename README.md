# Connect4

### Description
Connect 4 game where you one players plays against the computer. It's based on Min-Max algorithm (with and without pruning) where the player choose the K value and whether to perfrom pruning or not.

### How to play
The game is implemented in python 3.7 so you must have python interpreter and run the code.<br>
When you run the code you this window will appear:<br><br>
![image](https://user-images.githubusercontent.com/61145262/155901430-76305682-cef3-4ae2-82d8-bf1a98fce03c.png)<br>
You will choose the K value. The higher the k value the smarter the computer but it will take more time to finish execution and make the move(In general the K value is the number of moves that the computer looks ahead in order to make the best move using the Min-Max algorithm).<br>
Pruning is a technique which is used to make decision fatser(It cuts large parts of the tree which is unencessary in making the desicsion).<br><br>
Then you will head to the next window where you play against the computer:<br><br>
![image](https://user-images.githubusercontent.com/61145262/155901627-b7f62304-ba9c-4da5-8a24-a332050782ce.png)<br>
The player is the yellow one and the computer is the red one and you will drop pieces just by moving to the place you'd like and click to drop the piece.

### Technical information:
At each step, you will find in the console the execution time and the number of nodes expanded.<br>
![image](https://user-images.githubusercontent.com/61145262/155901753-7210e8a5-890c-45bb-b737-97bc047de4d5.png)<br>

#### Heuristic function:
The heuristic function as following :
* It adds 1000 when 4 pieces are made in any direction.
* It adds 100 when 3 pieces are made in any direction.
* It adds 5 when 2 pieces are made in any direction.
* It prioritize the mid columns by puting more wights on the mid columns also in the mid rows(Moves in the middle are better).
* It subtracts the same quantity if the user is the one whomake these moves.

#### Log file:
The program used log file which was primarely used in debugging the program. You will find log.txt file created where there is the board followed by its heuristic socre(When you find 1000000000 or -1000000000 it means that this branch was pruned).
