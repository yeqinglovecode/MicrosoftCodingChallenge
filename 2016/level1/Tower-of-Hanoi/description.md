This is a simple Tower of Hanoi problem.

You will be given 3 Pegs (or vertical stands) and N disks stacked on any one of the Pegs (the 1st Peg in this example). Each disk is of different diameter and has a hole in the center.

Your job is to move the Pegs from the Source peg to the Destination Peg while following the two rules below, and return the minimum number of moves it takes to do so:

Rule 1: You can only move exactly 1 disk at a time (from any peg to any other peg).

Rule 2: You may not stack a larger disk on top of a smaller one.

You may use the left over peg for temporary storage.

Example: int TowerOfHanoi(numberOfDisks, fromPeg, toPeg)

   <|>          |               |
  <<|>>         |               |
 <<<|>>>        |               |
---------   ---------      ----------
Peg 1       Peg 2           Peg 3
In this example, you have to move 3 disks from Peg 1 to Peg 3. Hence, Peg1 is the source or 'fromPeg'. Peg 3 is the desination or 'toPeg' and Peg 2 is the help peg for temporary storage of disks. Disks can be moved as below, where each line represents the movement of the topmost Disk from Peg -> Peg, without ever placing a large disk over a small one.

1 -> 3                  
1 -> 2
3 -> 2
1 -> 3
2 -> 1
2 -> 3
1 -> 3  
After the move is complete, you should return the minimum number of moves the full operation took: 7 in this case.

Note: If the Disks are moving to the Same Peg, the output should be 0; that is, from Peg2 to Peg2 there will be 0 moves.

You can assume that Number of Disks will be in the range of 1 to 15, inclusive. Also, the number of pegs is fixed at 3.

Input definition

Each lines will contain 3 non-negative integers in the order below: numberOfDisks, fromPeg, toPeg

There can be any number of lines and a "\n", "\r", or line break after each line. There is also a line break at the end of the Input.

Output definition

Output should have the same number of lines (rows) as input. Each output row must contain a non-negative integer indicating the minimum number of moves it takes to complete the TowerOfHanoi operation in the corresponding input line. Each line of integer output, including the last one, should end with a line break.

Example input

3,1,2
7,1,3
5,1,2
Example output

7
127
31
