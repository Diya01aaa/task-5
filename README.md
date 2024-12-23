# task-5
ROCK, PAPER AND SCISSORS  Write a simple game of Rock, Paper, Scissors where the user plays against the computer.
import random

# Function to determine the winner
def determine_winner(user_choice, computer_choice):
    if user_choice == computer_choice:
        return "It's a tie!"
    elif (user_choice == "rock" and computer_choice == "scissors") or \
         (user_choice == "scissors" and computer_choice == "paper") or \
         (user_choice == "paper" and computer_choice == "rock"):
        return "You win!"
    else:
        return "Computer wins!"

# Main game loop
print("Welcome to Rock, Paper, Scissors!")
choices = ["rock", "paper", "scissors"]

while True:
    # Get user's choice
    user_choice = input("Enter your choice (rock, paper, scissors or 'quit' to exit): ").lower()
    
    if user_choice == "quit":
        print("Thanks for playing! Goodbye!")
        break
    elif user_choice not in choices:
        print("Invalid choice. Please choose 'rock', 'paper', or 'scissors'.")
        continue
    
    # Get computer's choice
    computer_choice = random.choice(choices)
    print(f"Computer chose: {computer_choice}")
    
    # Determine the winner
    result = determine_winner(user_choice, computer_choice)
    print(result)
