# -project-3
import random

def computer_guesses():
    print("Welcome to 'Guess the Number'!")
    print("Think of a number between 1 and 100, and I'll try to guess it.")
    print("You need to guide me by responding with 'too high', 'too low', or 'correct'.")
    
    low = 1
    high = 100
    attempts = 0

    while True:
        attempts += 1
        if low > high:
            print("It seems like there's an issue with the responses. Let's restart!")
            break
        
        # Computer's guess
        guess = random.randint(low, high)
        print(f"My guess is: {guess}")
        
        # User input
        response = input("Is it 'too high', 'too low', or 'correct'? ").lower()

        if response == "too high":
            high = guess - 1
        elif response == "too low":
            low = guess + 1
        elif response == "correct":
            print(f"Yay! I guessed your number {guess} in {attempts} attempts!")
            break
        else:
            print("Invalid response. Please reply with 'too high', 'too low', or 'correct'.")

# Run the game
computer_guesses()
Welcome to 'Guess the Number'!
Think of a number between 1 and 100, and I'll try to guess it.
You need to guide me by responding with 'too high', 'too low', or 'correct'.
My guess is: 11
Is it 'too high', 'too low', or 'correct'? 11
