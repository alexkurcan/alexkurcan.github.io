## Guessing Game

```mermaid
flowchart TD
Start([Begin])
Start --> RanNum{numbertoguess= random number from 1-20}
RanNum --> user_input[/ask user to input guess/]
user_input --> intcheck[Run an integer check on the user input]
intcheck --> int_false[False]
int_false --> outfal[/Your input is not an integer!/] --> user_input
intcheck --> int_true[True] --> numcheck[Run a check if user input is the right number]
numcheck --> incor[False]
incor --> hicheck[Check if user input > the number]
hicheck --> hitrue[True] --> too_high[/Too high!/]
too_high --> user_input
hicheck --> hiflase[False] --> too_low[/Too low!/] --> user_input
numcheck --> numtru[True]
numtru --> isnum[/You guessed the number, congrats!!/]
isnum --> End([End])

```

### Documentation Section
This flow chart, then, essentially illustrates the procedure that the program would follow if it were written in code. As you can see, it includes a loop that illustrates what would happen if the user made an incorrect guess, in which case the process would restart and require a new input value. Subsequently, there is the higher or lower feature, which functions as a loop to indicate that there will always be a higher or lower feature to assist the user in guessing the correct number by gradually drawing nearer to their guess (with the higher or lower feature assisting them in finishing the task of determining the number). Naturally, if they correctly guess the number, then everything is OK and the cycle concludes with a little message congraluating them. And if they still are not able to guess the correct number than the loop contuines along with the higher or lower feature running, to again assist them within the game, until they do evenutally guess the the number.