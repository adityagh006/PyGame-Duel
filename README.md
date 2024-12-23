# Multiplayer Rock Paper Scissors Game
A networked multiplayer implementation of Rock Paper Scissors using Python, Pygame, and socket programming. Players can compete in real-time over a local network.


## Features
- Real-time multiplayer gameplay
- Client-server architecture
- Interactive GUI using Pygame
- Match result display
- Waiting room functionality
- Game state synchronization


## Prerequisites
- Python 3.x
- Pygame library
- Socket library (built into Python)
- pickle library (built into Python)


## Installation
1. Clone the repository:
```bash
clone https://github.com/yourusername/multiplayer-rps.git
```
2. Install the required dependencies:
```bash
pip install pygame
```


## Project Structure
```
multiplayer-rps/
│
├── server.py          # Server implementation
├── client.py          # Client and GUI implementation
├── network.py         # Network communication handler
├── game.py           # Game logic and state management
└── README.md         # Documentation
```


## Running the Game
1. Start the server:
```bash
python server.py
```
2. Launch the client(s):
```bash
python client.py
```
Note: You need to run at least two client instances to play the game.


## Network Configuration
By default, the game runs on:
  - Host: localhost
  - Port: 5555

To play over LAN:
  1. Change the server address in network.py to your server's IP address
  2. Ensure the port 5555 is open on your network


## How to Play
1. Launch the server
2. Start two client instances
3. Click "Click to Play!" on both clients
4. Choose your move (Rock, Paper, or Scissors)
5. Wait for both players to make their moves
6. Results will be displayed automatically


## Game Controls
- Mouse click to select moves
- Close window to exit game


## Technical Details
### Server (server.py)
  - Handles multiple game instances
  - Manages client connections
  - Synchronizes game state

### Client (client.py)
  - Implements the GUI using Pygame
  - Handles user input
  - Displays game state


### Network (network.py)
  - Manages socket connections
  - Handles data serialization
  - Implements client-server communication


### Game Logic (game.py)
  - Implements game rules
  - Tracks game state
  - Determines winners
