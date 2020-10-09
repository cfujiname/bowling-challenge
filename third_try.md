## AFTER PROCESS REVIEW

# Objectives

_Count and sum the scores of a bowling game for one player_


-------------------
INPUT        |    OUTPUT

20.times 1         20


- This is the simplest problem in the whole challenge
- So if I input 20 rolls of 1 pin down, my game should equal 20
- Where do I store the pins down? Initialize an array @rolls, then insert all pins down to that array
- Unit test: create a new game, add roll(pins), expect the _score_ to equal 20
- Rspec, no method score
- Create method score, hard code first output 20 to make tests pass
- But if I want my score to be counted related to number of rolls and pins down, I have to change my method _score_ to be able to count how many rolls and the referred pins down
- So, in my method _score_, I add _total_, so I can show the total points, which is my rolls array all summed up



- Same methodology for testing a _gutter game_

_Gutter Game_

INPUT        |    OUTPUT

20.times 0          0

-------------------

- because I don't want my score to be hardcoded, I need to find another case in the challenge that gives me the possibility of changing the score into a more 'scorish' style






 








# Game structure
Strike = 10 pins down in the first roll of frame (no more rolls allowed)

Strike Bonus points => Points from frame =+ 1 (in the 2 rolls)

Spare = 10 pins down in two rolls (i.e. 4 pins in 1st roll, 6 pins in 2nd roll)

Spare Bonus points => Points from frame =+ 1 (in the 1st roll)

10th frame => if Strike or Spare

10Strike => 10 pins down in the first roll of frame, plus 2 extra rolls and it’s points (Points = 10 + n + m)
10Spare => 10 pins down in two rolls (i.e. 4 pins in 1st roll, 6 pins in 2nd roll) and points for 1 extra  roll (Points = 4+6, plus i.e.5)

Gutter Game = zero points, never hits pins
- User inputs 0 


Perfect Game = 300 points (12 Strikes - 10 * 10 for normal frame strikes, plus points from one subsequent rolls(because it is a strike),  and 10 * 2 for extra rolls)