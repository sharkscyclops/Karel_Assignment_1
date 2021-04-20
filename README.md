# Karel_Assignment_1
#1/7 Karel Assignments

from karel.stanfordkarel import *

"""
File: PuzzleKarel.py
--------------------
Karel should finish the puzzle by picking up the last beeper (puzzle piece) and placing it in the right spot.
Karel should end in the same position Karel starts in -- the bottom left corner of the world.
"""

def main():
    move_and_pickup()
    put_puzzle_in_place()
    return_home()

def move_and_pickup():
    move()
    move()
    pick_beeper()

def put_puzzle_in_place():
    move()
    turn_left()
    move()
    move()
    put_beeper()

def return_home():
    turn_left()
    turn_left()
    move()
    move()
    turn_right()
    move()
    move()
    move()
    turn_left()
    turn_left()
    #turn_left()
    #turn_left()

def turn_right():
    for i in range (3):
        turn_left()    

if __name__ == '__main__':
    run_karel_program('Puzzle.w')
