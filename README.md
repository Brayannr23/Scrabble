Scrabble

A C program that scores two Scrabble words and reports which player wins, written for CS50's Problem Set 2.

What it does
Prompts each player for a word
Scores each word by adding up the point value of every letter (standard Scrabble letter values)
Ignores spaces, digits, hyphens, and any other non-letter character (they score 0)
Treats uppercase and lowercase letters the same
Prints Player 1 wins!, Player 2 wins!, or Tie!
Example
$ ./scrabble
Player 1: COMPUTER
Player 2: SCIENCE
Player 1 wins!
How it works

Letter values are stored in a 26-element array, POINTS, indexed by each letter's position in the alphabet (A = 0, B = 1, ... Z = 25). For any uppercase letter, subtracting the ASCII value of 'A' gives that position directly, which is used as the index into POINTS.

Scoring logic lives in a single function, compute_score, which main calls once per player, so the scoring loop is written only once.

Building and running
make scrabble
./scrabble
