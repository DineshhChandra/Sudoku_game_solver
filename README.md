# Sudoku_game_solver
The game is to fill a 9x9 grid with digits such that each row, column and 3x3 section contain number between 1 and 9, with each number used only once in each section 
The grid is partially filled intitally.
It requires some logic and reasoning, it also helps to improve your concentration and logical thinking.
It is solved using Pure Backtracking algorithm. 
In the pure backtracking solution, we iterate through the matrix and whenever an empty box is found, we assign a digit to the box, where such digit is not present in the current column, row, and 3×3 submatrix. 
After assigning the digit to the current cell, we recursively check whether this assignment leads to a valid solution or not. 
If the assignment doesn’t lead to a valid solution, then we try the next valid digit for the current empty cell. And if none of the digits leads to a valid solution, then the instance is not possible.
We can decrease the time complexity of the backtracking code using Bit masks.
For each box,row,column create a bitmask and for each element in the grid set the bit position = 1 in the corresponding bitmasks.
Each time we add/remove an element to/from the grid set the bit to 1/0 to the corresponding bitmasks.
