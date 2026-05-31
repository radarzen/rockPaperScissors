# Pseudo-code for the Rock Paper Scissors game.

1. Initialize Constants and Variables
   1. Computer Choice Constant {computerSelection}
   2. User Choice Constant {humanSelection}
   3. Computer Score {computerScore}
   4. User Score {humanScore}
   5. Game Loop Counter {gameLoop}
   6. Winner of Round {roundWinner}
2. Create Computer Choice function {getComputerChoice}
   1. Choose random number 1-3
   2. Return {computerChoiceVar}
3. Create Human Choice function {getHumanChoice}
   1. Prompt user for choice (rock, paper, scissors), assume valid input for now
   2. Convert user input to lowercase
   3. Convert user choice to number (1=rock, 2=paper, 3=scissors)
   4. Return {humanChoiceVar}
4. Create function to play a single round {playRound}
   1. Set const computerSelection to getComputerChoice
   2. set const humanSelection to getHumanChoice
   3. Calculate Winner:
      1. if computerSelection === humanSelection
         1. end turn in draw
      2. else if computerSelection === 3 && humanSelection === 1
         1. humanScore + 1
      3. else if computerSelection === 1 && humanSelection === 3
         1. computerScore + 1
      4. else if computerSelection > humanSelection
         1. computerScore + 1
      5. else computerSelection < humanSelection
         1. humanScore + 1
      6. Convert winner number to name (1=rock, 2=paper, 3=scissors)
      7. Output winner, loser, and the final score
      8. Return roundWinner
5. Start loop for gameLoop times
   1. Call playRound
   2. Update computerScore or humanScore based on roundWinner
   3. Increment gameLoop   
6. End loop
8. Calculate winner:
    1. If computerScore < humanScore
       1. Display "You win!  You're a winner!"
    2. If computerScore > humanScore
        1. Display "You lose.  You're a loser!"
    3. If computerScore === humanScore
        1. Display "It's a tie!"
