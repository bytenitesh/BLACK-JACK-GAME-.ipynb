
# Blackjack Game

Welcome to the **Blackjack Game**! This project is a classic implementation of the popular card game Blackjack (or 21) using Python. It's built using object-oriented programming principles, making the code clean and modular.

## Features

- **Object-Oriented Design**: The game is structured using classes such as `Card`, `Deck`, `Hand`, and `Chips` for a clean and modular design.
- **No GUI**: The game runs in the console, providing a raw coding experience.
- **Basic Game Logic**: Includes shuffling, dealing cards, adjusting for aces, and handling bets.
- **Simple and Fun**: Easy to understand and play.

## Getting Started

### Prerequisites

- Python 3.x

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/blackjack-game.git
    ```
2. Navigate to the project directory:
    ```sh
    cd blackjack-game
    ```

### How to Play

1. Run the game script:
    ```sh
    python blackjack.py
    ```
2. Follow the on-screen prompts to play the game.

## Game Classes and Their Responsibilities

- **Card**: Represents a single card in the deck.
- **Deck**: Represents the deck of cards, includes methods for shuffling and dealing.
- **Hand**: Represents the player's or dealer's hand, includes methods for adding cards and adjusting for aces.
- **Chips**: Represents the player's chips, includes methods for handling bets.

## Code Overview

Here's a brief look at the structure of the main classes:

```python
class Card:
    def __init__(self, suit, rank):
        self.suit = suit
        self.rank = rank

    def __str__(self):
        return f"{self.rank} of {self.suit}"

class Deck:
    def __init__(self):
        self.deck = [Card(suit, rank) for suit in suits for rank in ranks]

    def shuffle(self):
        random.shuffle(self.deck)

    def deal(self):
        return self.deck.pop()

class Hand:
    def __init__(self):
        self.cards = []
        self.value = 0
        self.aces = 0

    def add_card(self, card):
        self.cards.append(card)
        self.value += values[card.rank]
        if card.rank == 'Ace':
            self.aces += 1

    def adjust_for_ace(self):
        while self.value > 21 and self.aces:
            self.value -= 10
            self.aces -= 1

class Chips:
    def __init__(self):
        self.total = 100
        self.bet = 0

    def win_bet(self):
        self.total += self.bet

    def lose_bet(self):
        self.total -= self.bet
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to the Python community for their invaluable resources and tutorials.

---
