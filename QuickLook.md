# Purpose

I juggle many projects on (and off) github. But if you want to get a taste for what I've been working on, here are a few of my favorites:

# Flip Dot Puzzle

My first ever original [Twisty Puzzle](https://en.wikipedia.org/wiki/Combination_puzzle), which I named the Flip Dot Puzzle, was designed in Solidworks.
Before creating the puzzle, I designed a simulator in MatLab out of fear that I'd be unable to solve the puzzle once I'd assembled it.
My student license to both of these programs has since expired, but since my original design had some flaws,
I decided to recreate both the simulator (in python, on the Spyder IDE), and the CAD model (in OnShape).

These are pictures of my original Flip Dot Puzzle, which I 3D printed using the makerspace at the University of Pittsburgh.

[solved]()
[scrambled]()

In my redesign, I...
* made matching colors closer to each other in the solved state (for more visual clarity to the solver)
* reshaped parts to correct for slight misalignments when turning the puzzle
* changed the shape of the dots to make stickers easier to apply
* implemented a mechanism so prevent the central screw from loosening during the operation of the puzzle
* slightly altered dimensions, especially to thicken some parts that were unnecessarily thin

[Feel free to view the CAD model of my redesign on OnShape](https://cad.onshape.com/documents/6d13049500a96a43bc1b0cea/w/c66486e3c31c34519027e35c/e/2db2d1c96ce384fada7534fc)

The updated simulator of my FlipDot puzzle can be found [here]().

# Pentultimate

This is not an original puzzle like my Flip Dot Puzzle (The Pentultimate was invented by Jason Smith, and published
[here](http://twistypuzzles.com/forum/viewtopic.php?f=9&t=9195)),
but it's one of my favorite puzzle geometries, and I wanted to see if I could recreate the puzzle on my own.

My design is currently unfinished, but progress is promising.

## Next Steps

Right now, I'm trying to learn Featurescript so I can make a program to perform multiple Split commands at once.
This should make designing the Pentultimate -- and future twisty puzzles -- far more efficient for me.

[This is my CAD model for the Pentultimate Puzzle](https://cad.onshape.com/documents/e7bbb94138d107424aac71d4/w/6089e5dd90d7c048e1b93003/e/647c630bfbed9b9dd7119bcd)

# Split Decisions

My favorite word puzzle is the [Split Decisions](http://www.split-decisions.us/) puzzle. It's similar to a crossword,
but it relies on objective spellings rather than subjective clues.

I've created tools to help me design a Split Decisions puzzle that I could proudly present to my friends. These tools are:
* [a Python Script to quickly make a word bank of Split Decisions word pairs from a large .txt file of ordinary words](https://github.com/sht90/split-decisions/blob/main/SplitDecisionsFinder.py)
* [a Python Script to print a professional-looking image of a Split Decisions board](https://github.com/sht90/split-decisions/blob/main/DisplayBoard.py)
* [a Python Script to find shared words between two large text files](https://github.com/sht90/split-decisions/blob/main/Merge_txt_files.py)

Using these scripts, the only work I would have to do would be to pick which words I'd like to choose from
(usually I just pick the 10000 most common English words, and then prune out the ones that aren't found in the official Scrabble dictionary),
create a word bank out of all the possible Split Decisions word pairs from those words, make a .txt file of a board using those words / word pairs, and then
print it.

This was a fun coding challenge. I had basically never done any GUI or image generation before, so this was a great start.
Plus, I'm proud that I was able to generate a word bank in O(nlgn) instead of O(n^2).

However, I can only make puzzles for my friends -- not myself. Ideally, I'd be able to randomly generate a valid puzzle, which I could solve myself.

## Next Steps

I'm working on randomly generating a Split Decisions board. I decided to use C++, since generating a random Split Decisions board seemed like a 
recursive backtracking problem, and pointer/reference tricks can make my C++ implementation way faster than my python implementation would've been.
