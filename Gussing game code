import random

def get_limit(): """Gets a valid positive integer limit from the user.""" while True: try: limit = int(input("Enter the limit: ")) if limit > 0: return limit else: print("Please enter a positive number.") except ValueError: print("Invalid input. Please enter a whole number.")

def play_game(): """Plays one round of the Guess the Number game.""" limit = get_limit() secret_number = random.randint(1, limit)

print(f"I'm thinking of a number from 1 to {limit}")

tries = 0
guess = None

while guess != secret_number:
    try:
        guess = int(input("Your guess: "))
        tries += 1
        
        if guess < 1 or guess > limit:
            print(f"Guess must be between 1 and {limit}.")
            # Don't count this as a real attempt
            tries -= 1 
            continue 
        
        if guess < secret_number:
            print("Too low.")
        elif guess > secret_number:
            print("Too high.")
        
    except ValueError:
        print("Invalid input. Please enter a whole number.")
        # Don't count this as a real attempt
        tries -= 1

print(f"You guessed it in {tries} tries.")
--- Main Game Loop ---
print("Guess the number!") playing = True while playing: play_game()

while True:
    play_again = input("Would you like to play again? (y/n): ").lower()
    if play_again in ['y', 'n']:
        break
    else:
        print("Invalid choice. Enter 'y' or 'n'.")
        
if play_again == 'n':
    playing = False
print("Bye!")
