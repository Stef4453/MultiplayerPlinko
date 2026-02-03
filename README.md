# Plinko Royale

A physics-based multiplayer battle royale inspired by classic Plinko mechanics. Players compete in rounds of ball-dropping action to be the last one standing.

## Game Presentation

Plinko Royale is a real-time multiplayer game built with Matter.js for physics and Ably.io for networking. It features high-stakes point management, progressive difficulty and more. The game scales across desktop and mobile devices, allowing for seamless cross-play.

## Game Rules

### Objective
The goal is to survive all rounds by maintaining a positive point balance. If your points drop below 10, you are eliminated.

### Rounds and Difficulty
The game progresses through 16 rounds with increasing difficulty levels:
- Easy (Rounds 1-2): Standard 8-row peg board.
- Medium (Rounds 3-4): 12-row peg board for more variance.
- Hard (Rounds 5-6): 16-row board with obstacles where balls can get stuck.
- Insane (Rounds 7-11): Same as Hard, but with lower chances of multiplying points and trickier obstacles.
- Impossible (Rounds 12-16): Worse chances of multiplying points and some obstacles in the middle where balls can get stuck easily.

### Gameplay Mechanics
- Each player starts with 1000 points.
- Players take turns dropping a ball from the top of the board.
- Before dropping, players must choose a risk amount (minimum 10 points).
- The ball hits pegs and obstacles as it falls into bins with different multipliers.
- Your points are updated based on the multiplier of the bin the ball lands in.
- Elimination: Players with less than 10 points cannot take their turn and are marked as OUT.
- Victory: The last player with points remains the winner. If multiple players survive Round 16, the one with the highest points wins.

### Spectating
Players joining a game already in progress enter as Spectators. They can watch the current match and will be automatically added as active players when the next game starts.
**KNOWN BUG: Players who don't click "OK" in the "Game Finished" screen before the host starts a new game will not be added to the next game.

## Admin Commands

The game includes a set of debug commands accessible via the browser developer console (F12). Note: Most destructive commands require you to be the Host.

To see all available commands, type into the console:
`PlinkoAdmin.help()`

### Common Commands:
- PlinkoAdmin.listPlayers(): View all players, their current points, and their unique IDs.
- PlinkoAdmin.setPoints(index, amount): Set the point balance for a specific player by their list index.
- PlinkoAdmin.setRound(number): Instantly jump to a specific round to test different difficulty tiers.
- PlinkoAdmin.forceWin(index): End the current game immediately and declare a specific player the winner.
- PlinkoAdmin.shutdown(): Force a session-wide reload for all players to clear the room.

## Have fun playing and make sure to send me any bugs you may find in the game! Remember: this is just a project made for fun, so I won't be able to fix everything too fast.
Plinko Multiplayer. Vibe-Coded by Stef using Antigravity.
