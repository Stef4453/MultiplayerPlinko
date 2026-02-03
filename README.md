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
- Hard (Rounds 5-6): 16-row board with moving obstacles.
- Insane (Rounds 7-11): 16-row board with rotating red bricks.
- Impossible (Rounds 12-16): Adds "X0" center dividers that void your drop points entirely.

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

## Technical Details

- Physics Engine: Matter.js
- Networking: Ably.io Realtime Messaging
- Frontend: HTML5, CSS3 (Vanilla), JavaScript (ES6+)
