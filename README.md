# Python Blackjack Game

A simple command-line blackjack game implemented in Python.

## Features
- Single-player gameplay against the dealer
- Visual card representation in the terminal
- Chip-based betting system (white $1, red $5, green $25, black $100, purple $500, orange $1000)
- Account balance tracking with transaction history
- Interactive gameplay with options to hit, stand, or double down

## Installation

1. Clone this repository:
```bash
git clone https://github.com/dynamic-stall/blackjack-python.git
cd blackjack-python
```

2. Create and activate the conda environment from the provided file:
```bash
conda env create -f environment.yml
conda activate blackjack
```
- (Refer to my [aws-iam-credential-report](https://github.com/dynamic-stall/aws-iam-credential-report/) repo for Miniconda installation assistance, if Python is not present on your system.)

3. Install required packages:
```bash
pip install -r requirements.txt
```

## Project Structure
```
blackjack-python/
├── __init__.py
├── account.py          # Account management for betting
├── card_components.py  # Card, Deck, and Hand classes
├── constants.py        # Game constants (cards, chips)
├── environment.yml     # Conda environment configuration
├── game.py             # Main game logic
├── main.py             # Entry point
├── players.py          # Player and Dealer classes
└── README.md           # (This file)
```

## How to Play

1. Run the game directly:
```bash
python3 main.py
```

2. Enter your name when prompted

3. Place bets using chip colors:
   - Format: "[number] [color] [number] [color] ..."
   - Example: "2 black 1 green" for $225 ($100 x 2 + $25)

4. Game Actions:
   - `hit`: Draw another card
   - `stand`: Keep current hand
   - `double`: Double your bet and receive one more card (only available on initial hand)

5. Win Conditions:
   - Get closer to 21 than the dealer without going over
   - Dealer busts (goes over 21)
   - Initial two cards totaling 21 (Blackjack)

## Note
This game uses pandas for transaction tracking. Make sure you have it installed via the ```requirements.txt``` file.

## Future Improvements (at some point...)
- Multiple player support
- Split pairs option
- Insurance bets
- Save game progress
- Statistics tracking