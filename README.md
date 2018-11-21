# HexapawnAIGame ([Try It Here](https://www.cs.drexel.edu/~tmp346/upgratedHexapawnAIGame.html))
This is a simple game called Hexapawn Educable Robot described in [this article](https://www.gwern.net/docs/rl/1991-gardner-ch8amatchboxgamelearningmachine.pdf). The player will play against the computer. The computer learns from experience playing with the player to get better moves. This game gives a glimpse into some AI techniques.
## How To Play
As described in the article, Hexapawn is played on a 3 x 3 board, with three chess
pawns on each. Only two
types of move are allowed: (1) A pawn may advance
straightforward one square to an empty square; (2) a pawn
may capture an enemy pawn by moving one square diagonally,
left or right, to a square occupied by the enemy. The captured
piece is removed from the board. These are the same
as pawn moves in chess, except that no double move is permitted.
The game is won in any of three ways:
1. By advancing a pawn to the third row.
2. By capturing all enemy pieces.
3. By achieving a position in which the enemy cannot
move. 
## How It Works
- From the **original version** in the article, the computer simply remembers the board position it has faced and the moves associated with each board position in a memory. If the computer encounters any board position it has seen, it will choose randomly the next move on what is stored in memory. If it has not seen that board position before, it will get all the possible moves and randomly choose for the next move. If the computer loses, the last move will be deleted from the memory. If the computer wins, it will do nothing. It typically takes 16 losses for the computer to become undefeated.
- With the idea of the original version, I have created the **updated version** so that the computer learns faster. Other than just storing the move associated with the board position, the computer also stores the score for each move. The computer will choose the move with the highest score so far as its next move. If the computer wins, 1 point will be added to that move. If the computer losses, 1 point will be subtracted from that move. If that move score < 0, that move will be deleted from the memory. By using this technique, the computer learns much faster. It takes only 6 losses for the computer to become undefeated.
