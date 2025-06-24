# 🌽 Island Treasure – A Python Adventure Game

A simple text-based game built with conditionals and functions — perfect for Python beginners.

---

## 💡 What You Will Learn

* How to use `if/else` and `.lower()` to handle user input
* Building reusable functions in Python
* Game logic with conditional branching
* Creating replayable command-line apps

---

## 📖 About the Project

In *Island Treasure*, players explore a mysterious island in search of hidden gold. Each choice leads them deeper into the jungle or closer to danger. It’s a short and fun terminal game to reinforce decision-making logic in code.

---

## 🧠 The Code

```python
def game_over(reason):
    # This function ends the game and gives the player the option to try again.
    # 'reason' is a string passed in to explain why the game ended.

    print(f"\n{reason}")  # Display the reason for game over.
    print("💀 Game Over.")  # Game over message with emoji for visual effect.

    # Ask the player if they want to play again. 
    # .lower() makes the input lowercase to handle responses like "Yes" or "YES".
    play_again = input("Would you like to try again? (yes/no): ").lower()

    if play_again == "yes":
        start_game()  # Restart the game if player types "yes".
    else:
        print("Thanks for playing. Goodbye!")  # Exit message.
        exit()  # Stops the program completely so no more code runs.

def final_choice():
    # This function handles the final decision at the treasure room.

    print("\nYou find the treasure room. A voice whispers: take the gold or leave with your life?")

    # Prompt the player to choose between taking the gold or leaving.
    # Again, .lower() ensures case doesn't matter.
    choice = input("What do you do? (take/leave): ").lower()

    if choice == "take":
        # If the player chooses to take the gold, they lose because it’s cursed.
        game_over("The gold was cursed. You're trapped forever.")
    else:
        # If the player chooses to leave the gold, they win.
        print("You escape the island safely, wiser and richer in spirit. You win! 🏆")

def jungle_path():
    # This function runs when the player chooses to go into the jungle.

    print("\nYou push deeper into the jungle.")
    print("Left: a glowing plant 🌿")   # Presenting left path.
    print("Right: a dark cave 🕳️")     # Presenting right path.

    # Ask the player which direction they want to go.
    choice = input("Where do you go? (left/right): ").lower()

    if choice == "left":
        # If the player chooses left, they discover a helpful map and continue.
        print("You find a glowing map that leads to a hidden temple.")
        final_choice()  # Move to the final decision.
    else:
        # If the player chooses right, the cave collapses and they lose.
        game_over("The cave collapses around you.")

def start_game():
    # This function is the starting point of the game.
    # It sets up the scenario and presents the first major choice.

    print("\n🌴 Welcome to Island Treasure! Your mission: find the hidden gold.")
    print("You arrive on a mysterious island.")
    print("To your left: the jungle 🌳")
    print("To your right: the beach 🏖️")

    # Ask the player where they want to go first.
    choice = input("Where do you go? (left/right): ").lower()

    if choice == "left":
        # If the player chooses the jungle, continue the story.
        jungle_path()
    else:
        # If the player chooses the beach, they fall into quicksand and lose.
        game_over("You step into quicksand. You sink rapidly.")

# This part ensures the game starts only when the script is run directly,
# not if it's imported into another Python file.
if __name__ == "__main__":
    start_game()

```

---

## 🔍 Concepts in Action

| Concept                       | Where It Appears                            |
| ----------------------------- | ------------------------------------------- |
| Conditional Logic (`if/else`) | Throughout player decisions                 |
| Function Design               | Each scene is a self-contained function     |
| Input Sanitization            | `.lower()` ensures case-insensitive choices |
| Loops/Recursion               | Replay logic inside `game_over()`           |

---

## 🧹 Bonus Challenges

* Add a third path at the start (e.g., “mountains ⛰️”)
* Add health points or inventory tracking
* Include random elements using Python’s `random` module
* Track number of wins or losses across sessions

---

## ❓ Common Questions

**Q: Can I play this on Replit or an online IDE?**
A: Yes! Just copy the code into any online Python IDE and run it.

**Q: Does this work with Python 2?**
A: No. This game uses Python 3 syntax.

---

## ▶️ How to Run It

1. Make sure Python 3 is installed on your machine.
2. Clone this repository or copy the code into a file named `game.py`
3. In your terminal, run:

```bash
python game.py
```

---

## 🪪 License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).

---

🐍 This is part of the **Pythonly** beginner series. Learn Python one loop at a time.
Follow [@Pythonly](https://www.youtube.com/@Pythonly) for more.
