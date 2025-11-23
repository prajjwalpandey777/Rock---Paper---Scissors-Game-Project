# Rock---Paper---Scissors-Game-Project
#The most popular game of all time.


Description :-
            This Classic rock paper scisssor game is implemented in python programming


Features:- 
   1.Player vs. Computer gameplay.

   2.Clear instructions and user prompts.

   3.Input validation (handling incorrect input).

   4.Randomized computer moves.

   5.Display of the winner for each round.

Technologies used are 
     1.Python

Steps to play the game:-
 1.Enter the python programming code in the suitable platforms like vs code,google colab or jupyter notebook.
 2.Run the code and enter your choices from the given choices.
 3.Then the computer chooses a random choice against you .
 4.Then the result will be displayed based on your and computer selected choice.

Game code details = 

#Rock Paper Scissor

import random

options = ["rock", "paper", "scissor"]

while True: 
    user_choice = input("Choose rock, paper, scissor or quit :  ").lower() #This asks the user to enter a choice in the given choices
    if user_choice == "quit":
        print("Thanks for playing!")
        break #If the user choose to quit then the game quits and print "Thanks for playing!"
    if user_choice not in options:
        print("Invalid input.")
        continue #If ther user enter a choice which is not in the given choices then it prints "Invalid input."

    computer_choice = random.choice(options) #Here the computer randomly chooses a choice in the given choice against the user
    print(f"Computer chose: {computer_choice}")

    if user_choice == computer_choice: #If both user and computer chooses the same choice then it's a tie
        print("Tie!")
    elif (user_choice == "rock" and computer_choice == "scissor") or \
         (user_choice == "paper" and computer_choice == "rock") or \
         (user_choice == "scissor" and computer_choice == "paper"):
        print("You win!")
    else:
        print("You lose!")
    print("\nThanks for playing! \n")
