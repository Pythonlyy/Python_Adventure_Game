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
    print(f"\n{reason}")
    print("💀 Game Over.")
    play_again = input("Would you like to try again? (yes/no): ").lower()
    if play_again == "yes":
        start_game()
    else:
        print("Thanks for playing. Goodbye!")
        exit()

def final_choice():
    print("\nYou find the treasure room. A voice whispers: take the gold or leave with your life?")
    choice = input("What do you do? (take/leave): ").lower()  
    if choice == "take":
        game_over("The gold was cursed. You're trapped forever.")
    else:
        print("You escape the island safely, wiser and richer in spirit. You win! 🏆")

def spider_castle():
    print("\nSpiders surround you. Do you fight or run?")
    choice = input("Do you fight or run? (fight/run): ").lower()
    if choice == "fight":
        print("You survive the spiders. A river blocks your path.")
        choice = input("Swing across or take the bridge? (swing/bridge): ").lower()
        if choice == "swing":
            final_choice()
        else:
            game_over("The bridge snaps. You fall into the river.")
    else:
        game_over("You run, but the spiders are too fast.")

def jungle_path():
    print("\nYou push deeper into the jungle.")
    print("Left: a glowing plant 🌿")
    print("Right: a dark cave 🕳️")
    choice = input("Where do you go? (left/right): ").lower()
    if choice == "left":
        print("You find a glowing map that leads to the Spider Castle.")
        spider_castle()
    else:
        game_over("The cave collapses around you.")

def start_game():
    print("\n🌴 Welcome to Island Treasure! Your mission: find the hidden gold.")
    print("You arrive on a mysterious island.")
    print("To your left: the jungle 🌳")
    print("To your right: the beach 🏖️")
    choice = input("Where do you go? (left/right): ").lower()
    if choice == "left":
        jungle_path()
    else:
        game_over("You step into quicksand. You sink rapidly.")

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
