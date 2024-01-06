# Py Maze

Create and generate a maze, and then solve it using matplotlib.

Directions: 

Prologue: Ariadne's Thread
Ariadne, the daughter of Pasiphae and the Cretan king Minos, fell in love with Theseus, a Greek hero who came to Crete to slay the Minotaur, a monster half bull and half man that Minos kept in a subterranean labyrinth (maze). Ariadne gave Theseus a ball of yarn which he unwound as he entered the Labyrinth to slay the Minotaur. After slaying the Minotaur, Theseus followed the thread back to the entrance of the labyrinth and rejoined Ariadne.

In this assignment, we will implement a program that guides our hero Theseus through a randomly generated labyrinth to slay the Minotaur, leaving Ariadne's thread behind. We will represent the labyrinth with a numpy array, show it with matplotlib, and use recursion to help Theseus navigate through the labyrinth to find the Minotaur.

Chapter 1: The Labyrinth
In the first step, we will build and draw the labyrinth. Download the file maze.py Download maze.py(alternative download linkLinks to an external site.) and save it in the same folder as your file problem1.py. The file maze.py exports a function called generate(). When called, the function generates a new random maze and returns a tuple of three values: (width, height, plan). The values width and height are the dimensions of the maze. The value plan is a list of boolean values representing individual cells (squares) within the maze. If the value is True, the cell contains a wall. If it is False, the cell contains a corridor (passageway). The upper-left corner of the maze has coordinates [0, 0]. The entrance to the maze is always at the coordinates [0, 1].

The function takes the values returned by the maze generator and returns a two-dimensional Numpy array representing the labyrinth. Place Theseus at the entrance and Minotaur in the bottom-right corner at coordinates [-2, -2]. Use numpy.uint8 as the data type for the array and the following values to represent the content of each cell (square):

PATH     = 0  # The cell contains a passageway
WALL     = 1  # The cell contains a wall
THESEUS  = 2  # Theseus is in this cell
THREAD   = 3  # The cell contains Ariadne's thread
MINOTAUR = 4  # The Minotaur is in this cell
VISITED  = 5  # Special marker for the cells visited by Theseus

When you have the function implemented, generate a new maze, convert it to a labyrinth, and show the result with matplotlib.

The green square represents Theseus at the entrance and the yellow square represents the Minotaur.

Note: Both the Spyder editor and repl.it should be able to display the images generated by matplotlib. You can also develop your homework in a Jupyter notebook (the environment used in class) which is preinstalled in Anaconda. If you run into issues displaying the labyrinth and need help, please email Jan or one of the TAs and we will help you set it up. Also, don't worry about colors. Matplotlib selects colors automatically and it is fine if your color scheme is different from the example.

The function slay() will systematically explore the labyrinth until it finds the Minotaur. You can implement a very simple recursive search strategy in your slay() function. The search will start at the entrance and in each step it will recursively explore the adjacent cells (if possible). The search ends when the Minotaur is found. A path from the entrance to the Minotaur is guaranteed to exist (the generator ensures that).
