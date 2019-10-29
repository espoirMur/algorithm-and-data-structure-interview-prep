You are the owner of a coworking space like WeWork and your office building is rectangular. Your team just built wall partitions to create mini offices for startups. This office campus is represented by a 2D array of 1s (floor spaces) and 0s (walls). Each point on this array is a one foot by one foot square. You need to calculate the number of offices. A single office is bordered by walls and is constructed by placing floors next to each other, horizontally and/or vertically. Two 1s adjacent to each other horizontally or vertically are always part of the same office.


Functions
numOffices() has one parameter:

grid: a 2D grid/array of 1s and 0s

Input Format
For some of our templates, we have handled parsing for you. If we do not provide you a parsing function, you will need to parse the input directly. In this problem, our input format is as follows:

The first line is the number of rows in the 2D array
The second line is the number of columns in the 2D array
The rest of the input contains the data to be processed
Here is an example of the raw input:

4
5
11110
11010
11000
00000

Expected Output
Return the number of valid offices in the grid.


Constraints
Assume all four edges of the grid are all surrounded by walls.
Assume that the bounds of the array are the following:
The total amount of elements in the array: width x height <= 10^6

Example
Example numOffices() Input

grid: 
	[[1, 1, 0, 0, 0],
	 [1, 1, 0, 0, 0],
	 [0, 0, 1, 0, 0],
	 [0, 0, 0, 1, 1]]
Example Output

3
Solution

There's 3 offices in this grid, one made of four 1s on the top left, one made of one 1 in the middle, and one made of two 1s in the bottom right.
