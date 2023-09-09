# Create-a-game-where-the-computer-selects-a-random-number-and-the-player-has-to-guess-it.
import random

def guess_the_number():
    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        guess = int(input("Guess the number (1-100): "))
        attempts += 1

        if guess == secret_number:
            print(f"Congratulations! You guessed the number in {attempts} attempts.")
            break
        elif guess < secret_number:
            print("Try a higher number.")
        else:
            print("Try a lower number.")

guess_the_number()
