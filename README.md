Task Definition
The program checks whether a wall of a given configuration can be constructed using a provided set of bricks.

How the Algorithm Works

1. The input file contains:
Matrix size (width × height) and its content (0 - empty space, 1 - part of the wall).
Number of available brick types.
A list of bricks, formatted as (width, height, quantity).

2. The program calculates:
Total number of "1" cells in the matrix, representing the required wall area.
Total available brick cells, multiplying each brick's width, height, and quantity.

3. It then compares these values:
If the number of cells in the wall is less than or equal to the available brick cells → "yes" (the wall can be built).
Otherwise → "no" (not enough material to construct the wall).

Example Execution
Input File (input_1.txt - Expected Output: "no"):
The wall requires 16 cells.
Available bricks:
2×2, 1 piece (4 cells)
1×3, 1 piece (3 cells)
1×4, 1 piece (4 cells)
Total available: 4 + 3 + 4 = 11 cells.
11 < 16 → Output: "no".

Input File (input_2.txt - Expected Output: "yes"):
The wall requires 16 cells.
Available bricks:
2×2, 1 piece (4 cells)
1×3, 1 piece (3 cells)
1×4, 1 piece (4 cells)
3×4, 5 pieces (60 cells)
Total available: 4 + 3 + 4 + 60 = 71 cells.
71 > 16 → Output: "yes".

Implementation
Built using HTML + JavaScript.
The file is loaded via <input type="file">.
JavaScript processes the data and displays the result in <p id="output">.
