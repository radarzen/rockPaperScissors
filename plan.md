# Pseudo-code for the Rock Paper Scissors game.

1. Initialize Variables
   1. Computer Choice Variable {computerChoiceVar}
   2. User Choice Variable {humanChoiceVar}
   3. Computer Score {computerScore}
   4. User Score {humanScore}
   5. Game Loop Counter {gameLoop}
2. Create Computer Choice function {getComputerChoice}
   1. Choose random number 1-3
   2. Return {computerChoiceVar}
3. Create Human Choice function {getHumanChoice}
   1. Prompt user for choice 1-3 (1=R, 2=P, 3=S)
   2. Return {humanChoiceVar}
4. Start loop for gameLoop times
5. Call getComputerChoice
6. Call getHumanChoice (assume valid choice selected)
7. Calculate Winner:
   1. if computerChoiceVar === humanChoiceVar
      1. end turn in draw
   2. else if computerChoiceVar === 3 && humanChoiceVar === 1
      1. humanScore + 1
   3. else if computerChoiceVar === 1 && humanChoiceVar === 3
      1. computerScore + 1
   4. else if computerChoiceVar > humanChoiceVar
      1. computerScore + 1
   5. else computerChoiceVar < humanChoiceVar
      1. humanScore + 1
8. Display current score
9. End loop
10. Calculate winner:
    1.  If computerScore < humanScore
        1.  Display "You win!  You're a winner!"
    2.  If computerScore > humanScore
        1.  Display "You lose.  You're a loser!"
    3.  If computerScore === humanScore
        1.  Display "It's a tie!"
