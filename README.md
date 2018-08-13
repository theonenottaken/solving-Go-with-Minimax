# solving-Go-with-Minimax

#### Summary of Project

The program simulates the gameplay of the boardgame Go by taking the optimal turn for each player according to the minimax algorithm and then outputting the winner.
The program reads the current state of the game from an input file called “input.txt”. This file must reside in the current directory of the program executable. I’ve included
an example input file to use to run the program.

The board is a 5x5 grid, with E representing an empty tile, B representing a black controlled tile, and W representing a white controlled tile.
Black is assumed to be the next player to go. For each turn, the program uses a minimax graph of depth 3 (looks only 3 turns into the future) and chooses the optimal move based
on that perception. It does this for each player until the game is over and then outputs the winner to “output.txt” in the form of a single letter: B for black win and W for white
win.

For a better understanding of the minimax algorithm, see this link: https://en.wikipedia.org/wiki/Minimax

In short, each player chooses the move that will minimize his maximum loss – that is, choose the move such that the worst case scenario for him will be the least detrimental.

#### How to Run

On a Linux system, download the files so that they’re all in one directory. Open a terminal and `cd` to that directory. Type `make` and hit enter. Then type `./a.out` and hit enter.
That’s it! You should now find a new file in the directory called “output.txt”. The file contains a single letter indicating a black or white victory.
You will also have a new executable file called “a.out” in the directory, along with many object files. If you wish to run the program again without recompiling, leave these files in
the directory and just enter `./a.out` again in the terminal. If you wish to get rid of these generated files, enter `make clean`. 
