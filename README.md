Blackjack Blitz
Blackjack Blitz is a Python-based card game inspired by the classic Blackjack, featuring a unique "Sabotage" mechanic and a graphical interface built with Pygame. Compete against the dealer and other players to reach 21 without going bust—while using sabotage to tip the odds in your favor.

Features
Classic Blackjack Rules: Standard Blackjack card values and gameplay mechanics.

Multiplayer Support: 1 to 5 players can play in a single session.

Dealer AI: Dealer plays by standard casino rules (hits on ≤16, stands on ≥17).

Betting System: Players begin with a bank and place bets each round.

Sabotage Mechanic: Pay to force an eligible opponent to draw an additional card.

Graphical UI: Built using Pygame for visual card displays and game interaction.

Resource Management: Loads cards and icons from a Resources/ folder.

How to Play
Prerequisites
Python 3.x

Pygame library

Install Pygame via pip:

bash
Copy
Edit
pip install pygame
Running the Game
Ensure RMain.py and the Resources/ folder (with subfolders like Cards/ and Icons/) are in the same directory.

Run the main script:

bash
Copy
Edit
python RMain.py
Game Flow
Welcome Screen: Press RETURN to start.

Instructions: Review game rules. Press RETURN to proceed.

Select Players: Enter number of players (1–5), then enter each player's name.

Betting: Each player enters a bet for the round.

Gameplay:

Players receive 2 cards; the dealer gets one visible and one hidden card.

Players take turns to:

H - Hit: Draw a card.

P - Pass/Stand: Keep current hand.

S - Sabotage: Force an opponent to draw, at a cost (default $25).

Dealer's Turn: Dealer reveals their hand and plays according to rules.

Results:

Win if closer to 21 than the dealer or if the dealer busts.

Blackjack pays 2:1.

Tie (Push) returns the bet.

Next Round: Press RETURN to continue, or ESCAPE to exit.

Card Values
2–10: Face value

J, Q, K: 10

Ace (A): 1 or 11 (whichever is more favorable)

Code Structure
Card: A single card with suit, label, value, etc.

Deck: Creates, shuffles, and deals cards.

Dealer: Manages dealer-specific logic and deck control.

Player: Handles player stats, hand, bank, and decisions.

Additional utility functions manage the Pygame UI, text rendering, and game state.

Customization Options
Sabotage Cost: Change SABOTAGE_COST in RMain.py.

Sabotage Key: Change SABOTAGE_KEY to assign a different key.

Resource Files: Modify card images and icons in the Resources/ folder.

Winning Threshold: Adjust the winning_threshold value in the checkWinner() function.

Directory Structure
markdown
Copy
Edit
BlackjackBlitz/
│
├── RMain.py
├── README.md
└── Resources/
    ├── Cards/
    └── Icons/
Game Over Conditions
A player reaches the winning threshold (default: $500).

All players are out of money.

Enjoy playing Blackjack Blitz—where strategy meets sabotage!
