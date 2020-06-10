# Online Multi-player Snake Game

## Rules

- Snakes become longer by eating apples.
- Snakes with longer lengths can eat snakes with a shorter length.
- Snakes that try to eat longer snakes lose the game.
- Snakes that are eaten by other snakes lose the game.
- Last snakes who survives is the winner.
- Set a random Score for apples.
- Put random obstacles (stones) in the map where if a snake hits any of them, they lose.
- (extra point) implement bot for game

## Components

## Client

1. Your client must implement a boardgame*.
2. Your client must implement the required user interface for the server*.

*:  **Graphical user interface required**

### Notes: 
- You are free to use JavaFX.
- You are free to use any protocol or way to exchange the data between your server and the client.
- A user interface that is visually more beautiful has an extra point.

### Hints
- https://www.youtube.com/watch?v=vg2k24SuX5k
- https://winterbe.com/posts/2014/07/31/java8-stream-tutorial-examples/


## Server

1. Your server must support multi-user simultaneously (Multi-Thread Server).
2. Your server must provide a way to authenticate users.
3. Your server must provide a way for users to wait for other users to connect (lobby).
4. Your server must broadcast every user's move to other users in the game in real-time.
5. (extra point) Your server must have a Scoreboard and record user's Scores.
6. (extra point) Your server must record the game and show a replay of it later.
7. (extra point) Your server must support multiple games simultaneously.


Good Luck
