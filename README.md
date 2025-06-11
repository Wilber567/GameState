
# GameState

## Introduction

**GameState** is an esolang inspired by classic video game mechanics created by Wilber Escobar in 06/2026.  
The core idea behind this language is to simulate a video game through code—where each instruction represents an in-game event or action. Programs unfold like interactive narratives, allowing you to "play" through a sequence of game-like states and watch the story evolve as the code executes.

---

## Commands

| Description                                | Commands |
|--------------------------------------------|---------|
| Move the data pointer to the right         | **Move your piece!, March forward!, Shift right!, Proceed to the next room., Advance!, Go right!, Step ahead!, Onward!, Forward march!**    |
| Move the data pointer to the left          | **Back it up!, Let's rewind., Turn around!, Return to start., Retreat!, Backtrack!**    |
| Increment the value at the data pointer     | **Power up!, Level up!, Extra life!, 1-Up!, Gotta get stronger!, Get buffed!, Raise stats!, Gain XP!, Increase power!, Combo multiplier!, Collect bonus!, Boost activated!, Charging up!, Power increasing!, Energize!, Enhancing stats!, Skill leveled!, March forward!, Strength rising!, Stat boost!, Critical training!**    |
| Decrement the value at the data pointer     | **Oof!, You took damage!, Missed!, Lost a life!, Game Over!, Failed!, Hit!, Damage taken!, Lose a point!, Down you go!, Critical fail!, Setback!, Fall back!, Take a hit!, Hit confirmed!, Reduce power!, Health dropped!, Stat decrease!, Cooldown!, Weakness applied!, Penalty!**    |
| Output the value at the data pointer        | **Announce!, Cast spell!, Fire laser!, Reveal yourself!, Outputting data!, Read your score!, Display message!, Show result!, Data output!, Broadcast!, Signal sent!, Alert!**    |
| Input a value and store it at the pointer   | **Input received!, Player move!, Data input!, Command accepted!**    |
| Jump forward if the value is zero           | **Start a mini game!, Mission start!, Game on!, Ready? Fight!, Begin cursed incantation!**     |
| Jump back if the value is non-zero          | **End game phase!, Mission complete!, Game over!, Well done!**    |
| Set the value at the data pointer to 0      | **Resetting stats!, Back to square one!, Starting fresh!, Clear progress!, Resetting power!, Back to basics!, All cleared!, Rebooting!, Wasted.** |
| Multiply value at the data pointer by 5                     | **Multiply power!, Boost!, Power multiplied!, Max multiplier!** |
| Divide value at the data pointer by 2                       | **Split power!, Power reduced!, Strength split!, Reduced by half!, Cut in half!, Strength halved!, Power drained!** |
| Square the value at the data pointer      | **Power doubled!, Squared strength!, 2x Power!, Strength squared!, Squared boost!, Double trouble!, Amplified!** |
| Toggle the value at the data pointer between 0 and 1                     | **Flip switch!, Power flip!, Switch activated!, Mode switch!** |
| Set the value at the data pointer to maximum     | **Maxed out!, Power up to max!, Reach the top!, Maximum strength!, Top level reached!, Fully charged!, Maxed stats!, Overflow power!, Limit exceeded!** |
| Halve the value at the data pointer if greater than 100        | **Half of the beast!, Power reduction!, Strength split!, Cut the edge!, Decrease to a point!, Lowering force!, Strength diminished!** |
| Increase value at the data pointer by 11                    | **Big boost!, Massive power-up!, Tenfold increase!, Level 10 unlocked!, Big jump!, Strength surge!, Massive growth!, Jump in stats!** |

---

## Computational Class

**GameState** is Turing complete.


It can simulate a Turing machine, and its commands can be mapped to Brainfuck (BF) equivalents as follows:

| GameState                                                                 | Brainfuck Equivalent | Notes                                                 |
|--------------------------------------------------------------------------------|-----------------------|-------------------------------------------------------|
| Move your piece!, March forward!, Shift right!, Proceed to the next room., Advance!, Go right!, Step ahead!, Onward!, Forward march! | `>`                   | Move the data pointer to the right                   |
| Back it up!, Let's rewind., Turn around!, Return to start., Retreat!, Backtrack! | `<`                   | Move the data pointer to the left                    |
| Power up!, Level up!, Extra life!, 1-Up!, Gotta get stronger!, Get buffed!, Raise stats!, Gain XP!, Increase power!, Combo multiplier!, Collect bonus!, Boost activated!, Charging up!, Power increasing!, Energize!, Enhancing stats!, Skill leveled!, March forward!, Strength rising!, Stat boost!, Critical training! | `+`                   | Increment the value at the data pointer             |
| Oof!, You took damage!, Missed!, Lost a life!, Game Over!, Failed!, Hit!, Damage taken!, Lose a point!, Down you go!, Critical fail!, Setback!, Fall back!, Take a hit!, Hit confirmed!, Reduce power!, Health dropped!, Stat decrease!, Cooldown!, Weakness applied!, Penalty! | `-`                   | Decrement the value at the data pointer             |
| Announce!, Cast spell!, Fire laser!, Reveal yourself!, Outputting data!, Read your score!, Display message!, Show result!, Data output!, Broadcast!, Signal sent!, Alert! | `.`                   | Output the value at the data pointer                |
| Input received!, Player move!, Data input!, Command accepted!                | `,`                   | Input a value and store it at the data pointer       |
| Start a mini game!, Mission start!, Game on!, Ready? Fight!, Begin cursed incantation! | `[`                   | Jump forward past matching `]` if value is zero     |
| End game phase!, Mission complete!, Game over!, Well done!                   | `]`                   | Jump back to matching `[` if value is non-zero      |



---

## Example Programs

### Hello World
Collect bonus! Get buffed! Boost activated! Charging up! Collect bonus! 1-Up! Stat boost! Strength rising! Collect bonus! Critical training!
Game on!
Shift right!
Skill leveled! Power increasing! 1-Up! Combo multiplier! Energize! Enhancing stats! Extra life!
Advance!
Power increasing! Combo multiplier! Skill leveled! Increase power! Power increasing! Gain XP! Skill leveled! Get buffed! Extra life! Raise stats!
Move your piece!
Level up! 1-Up! Gotta get stronger!
March forward!
Combo multiplier!
Retreat! Back it up! Backtrack! Turn around!
Game Over!
Game Over!
Shift right!
Increase power! Enhancing stats!
Reveal yourself!
Go right!
Skill leveled!
Reveal yourself!
Boost activated! 1-Up! Skill leveled! Power up! Gain XP! Power up! Power up!
Read your score! Show result!
Strength rising! Raise stats! Extra life!
Read your score!
Forward march!
Power up! 1-Up!
Outputting data!
Let's rewind. Let's rewind.
Skill leveled! Increase power! Energize! Collect bonus! Extra life! Boost activated! Stat boost! Stat boost! Get buffed! Get buffed! Collect bonus! Charging up! Increase power! Raise stats! Extra life!
Signal sent!
Forward march!
Cast spell!
Combo multiplier! Gotta get stronger! Raise stats!
Outputting data!
Reduce power! Lost a life! Health dropped! Hit! Fall back! Lose a point!
Alert!
Oof! Oof! Game Over! Game Over! Damage taken! Damage taken! Failed! Take a hit!
Alert!
Go right!
Gotta get stronger!
Alert!
Onward!
Outputting data!

### Output the Input 10 times
Gain XP!
Shift right! Step ahead! Advance! Proceed to the next room. Onward! Advance! Step ahead! Step ahead! March forward! Step ahead!
Hit confirmed!
Start a mini game!
Input received!
Power increasing!
Ready? Fight!
Critical fail!
Reveal yourself!
Fall back! Lose a point! Lost a life! Cooldown! Hit! Critical fail! Setback! Health dropped! Take a hit! Lost a life!
Start a mini game! Begin loop!
You took damage!
Well done!
Move your piece!
Game over!
Let's rewind.
Hit!
Go right!
Game over!
Let's rewind.
Mission complete!

---
## External Resources
https://brainfuck.org
