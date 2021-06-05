## Multiplayer Snake Game Project
## Course: CSSE432 - Computer Networks
*Completed in Spring 2020-21*

**Please note that I cannot share the source code for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
Snake is a classic game in which the user controls a "snake" that wanders around the gameboard one time step at a time, growing in length each time it eats a piece of food, which is randomly re-generated on the board each time it is eaten. The snake dies if it hits any part of its own body, or the side of the game board, with its head. 

In this project, my team adapted this game to include multiple players simultaneously, with all players' games syncrhonized through communication with a central server that broadcasts all players' moves to each player's client application. The food is randomly generated and the location is broadcast to all clients when the previous food item was eaten, and a player's snake can die when hitting the side of the gameboard, or part of their own or any other player's snake. The high score is tracked across all players, and players may leave and rejoin the game at any time, with up to 4 players playing at the same time.

### My Contribution
For this project, I implemented all server-side code using Python sockets, as well as implementing the connection to the client snake applications written in Java. I also determined the communication protocol between the clients and server to allow for synchronization with up to 4 players at a time, and with players joining and leaving at any time. The communication protocol handled all communication about player moves, food locations, high scores, and all other information that needed to be shared with all clients. 

### Technical Architecture and Tools Used
*Programming Languages and Tools* <br>
Python - The server code was written in Python, using Python's socket libraries. <br>
Java - The client code, which contained the snake game logic as well as socket code to connect to the server, was implemented in Java. <br>
