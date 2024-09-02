# BlackJack Game - Python Implementation

## Overview

This repository contains a Python implementation of a simple BlackJack game. The game allows a player to play against a dealer (simulated by the program), with functionalities such as betting, insurance, and double down.

## Features

- **Deck Management**: A standard deck of 52 cards is used, shuffled at the beginning of each round.
- **Betting System**: Players start with a balance of $100 and can place bets each round. The game ends when the balance reaches zero.
- **Insurance Bet**: If the dealer's visible card is an Ace, players have the option to place an insurance bet to hedge against a potential BlackJack.
- **Double Down**: Players can choose to double their bet and receive exactly one more card.
- **Gameplay Options**: Players can choose to hit (draw another card), stand (end their turn), or double down during their turn.
- **Winner Determination**: The game determines the winner based on standard BlackJack rules and updates the player's balance accordingly.

## Classes and Methods

### `BlackJack` Class

- **Attributes**:
  - `deck`: List representing a standard deck of 52 cards.
  - `player_hand` & `dealer_hand`: Lists to hold the cards for the player and dealer.
  - `balance`, `bet`, `insurance_bet`: Manage player balance and bets.
  - `game_over`, `player_stand`, `dealer_stand`: Flags to manage game state.
  
- **Methods**:
  - `reset()`: Resets the game state, shuffles the deck, and deals initial cards.
  - `place_bet(amount)`: Places a bet and deducts it from the player's balance.
  - `place_insurance()`: Places an insurance bet if the dealer shows an Ace.
  - `double_down_bet()`: Doubles the bet and deals one additional card to the player.
  - `calculate_score(hand)`: Calculates the score for a given hand.
  - `update_balance()`: Updates the player's balance based on the game outcome.
  - `player_turn(action)`: Handles player's actions (hit, stand, double down).
  - `dealer_turn()`: Manages the dealer's actions following the player's turn.
  - `step(action)`: Advances the game state based on the player's chosen action.
  - `check_winner()`: Determines the winner based on final scores.
  
### `main()` Function

- The `main()` function initializes the game and manages the flow of play. It allows the player to place bets, make decisions, and view the outcome of each round. The game continues until the player either cashes out or runs out of balance.

## How to Play

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd blackjack-game
   ```

2. **Run the Game**:
   ```bash
   python blackjack.py
   ```

3. **Follow the Prompts**: 
   - Place your bet.
   - Choose your action (hit, stand, double down, or take insurance).
   - The game will display the outcome after each round.
   - Continue playing until you decide to cash out or your balance reaches zero.

## Requirements

- Python 3.x

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
