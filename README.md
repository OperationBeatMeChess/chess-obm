# Operation Beat Me ChessAI
## Overview
The goal of this project is to build and train a reinforcement learning chess engine capable of beating my friends and myself. This is will made in collaboration of Keith Gordan and myself. The readme will catalog the progess and directly we take to achieve this result. 

## Our goal
Our goal is simple, by combining our passion of low tier chess with our desire to learn more about applied machine learning. We aim to develop a mediocre Chess engine that can beat ourselves while simutaneously learning many new applicable skills for our future.

# The Project
## The Chess Board:
The first thing for this project will be devleoping a Chess board that has the key gym functions for reinforcement learning and a second enviroment which allows us to interact with the model through a chess GUI. 
## Self Play enviroment 
The self play enviroment requires our model to always think it is the entity playing. So our state must alternate its polarity to represent the side whos turn it is. we will let each piece be represented by a number and the number will be positive if it is that sides turn otherwise it will be negative.
| Piece  | Value it represents |
|--      |--                   |
| Pawn   | 1                   |
| Knight | 2                   |
| Bishop | 3                   |
| Rook   | 4                   |
| Queen  | 5                   |
| King   | 6                   |

now that we have the board represented in our state observation we want to add a little more information. The model needs to know the allowable moves in the position so we can filter out the invalid outputs of our model (Model output XOR possible moves). 

we want to leave the possibility to expand our enviroment by allowing our model to process variations to look ahead and build a tree representing the possible combition of moves to find the move with the best possible end result (look forward).
