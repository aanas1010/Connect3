# General Information

**Project Proposal:** AI for modified Connect Four

**Authors:** Aabid Anas, Matthew Chan, Shayaan Khan, Markus Nimi

# Problem Description and Research Question (300-400 words)

**Question: How can we create a simple Connect 4 AI and evaluate how well it plays?**
 
Connect Four, a board game invented in 1974, is a two-player game in which players take turns placing discs into a 6 by 7 matrix with the goal of connecting four of 
their discs vertically, horizontally, or diagonally before their opponent. The 7 columns are constrained by gravity, in that both players’ discs fall to the bottom of 
the column. This poses a limitation for players, allowing them a maximum of 7 possible moves per turn; if a column fills up, no more discs may be put into the column.
 
In order to make this project more computationally feasible, we decided to shrink the board into a 4 by 5 matrix in which 3 consecutive discs of the same colour result 
in a winner. 

Our goal in this project is to create a program that can gradually learn the game through trial and error. We can track different statistics regarding the choices of 
the AI to observe winning strategies and log the wins and losses to track the AI’s progress over time for a set amount of games. We then hope to be able to expand this 
application by allowing a human player to interact with the AI player. This way, we can easily test how practical the AI is against a player who can develop complex 
strategies rather than a simple random player.
 
We chose to pursue a project involving a game AI for a few reasons. By allowing the AI to mature over time, we forego the need for a large complex data set. As well, 
creating such an AI allows us to create the data set from scratch, allowing us to create custom abstract data types that fit all of our needs. This will make analyses 
much easier. Plus, we liked the idea of creating an AI from scratch as it shows the computational ability to work up from nothing.

# Computational plan (300-500 words)
**Game**

Initially, we will create an empty 4 by 5 game board for our game of Connect 3, with player red and player yellow, and yellow being the first player to start. Each side 
takes turns, dropping a disc into one of the 5 columns that has at least one free space. The columns fill from the bottom up, where each new piece in a column is stacked.
In our game representation, the elements of the list of lists will start with “O” for empty, then will correspond to “R” and “Y”, for red and yellow players respectively.
The game will have additional methods to change the state of the game, find out if the current state has a winner and find out if the state has any valid moves left.

**AI**
For this project, we will be using AIs with similar heuristics as those found in Assignment 2. In particular, we will be looking at the Exploring Player AI, which 
tends to have a greater win rate compared to other AIs in Assignment 2. In a similar fashion, we will make use of trees to track different games and their outcomes 
(that is, whether a game is a win, lose, or a tie). We will correspond each of these outcomes with a number (1.0, 0.0, and 0.5 respectively) being yellow-centric 
(that is, a “win” corresponds to a yellow victory, etc.), allowing us to aim for a yellow win or a red win, depending on which player the AI controls. Then, each 
subtree corresponding to a played game will have one of these scores applied to it; the generated master tree will then be used as a decision tree for our AI player.
 
**Interface and Interaction**
After a learning player is generated, the user will be able to view how the learning player does against a random player in a set number of matches. The number of 
games won and the percentage of games won will be shown to the user in the interface. Also, the user will be able to play a game against the learning player to test 
the effectiveness against a human. In order to play against the learning player, the interface must be able to display the game board and allow the user to insert 
pieces into the game board. The library Tkinter will be used to develop this interface. Tkinter is a python library that allows developers to create a graphical user 
interface.

# References

Berkeley GamesCrafters Research Group. “Connect 4.” GamesCrafters,
http://gamescrafters.berkeley.edu/games.php?game=connect4
 
“Connect Four.” F.G. Bradley’s, 1990,
https://www.fgbradleys.com/rules/Connect%20Four.pdf.
 
Weisstein, Eric W. “Connect-Four.” From Wolfram MathWorld,
mathworld.wolfram.com/Connect-Four.html.

