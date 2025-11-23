# Rock---Paper---Scissors-Game-Project
#The most popular game of all time.


import random
options = ["rock", "paper", "scissors"]
while True:
    user_choice = input("Choose rock, paper, or scissors? (or 'quit'): ").lower()
    if user_choice == "quit":
        print("Thanks for playing!")
        break
    if user_choice not in options:
        print(" Invalid input ")
        continue
    computer_choice = random.choice(options)
    print(f"Computer chose: {computer_choice}")
    if user_choice == computer_choice:
        print("Tie!")
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "paper" and computer_choice == "rock") or \
         (user_choice == "scissors" and computer_choice == "paper"):
        print("You win!")
    else:
        print("You lose!")
