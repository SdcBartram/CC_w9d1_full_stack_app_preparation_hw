# CC_w9d1_full_stack_app_preparation_hw

# Homework: Full Stack Games Hub App

## Questions

<img src="/dataflow_diagram.jpg">


1. What is responsible for defining the routes of the games resource?
The gamesRouter.js file is responsible for defining the routes of the games resource.

2. What do you notice about the folder structure? Whats the client responsible for? Whats the server responsible for?
The client and server are separate folders. Inside each are further separate folders for for components, containers, services, db and helpers. The client is responsible for the front end part of the application (components, containers and services). The server is responsible for the back end part of the application (database, route creator).

3. What are the the responsibilities of server.js?
The server.js is where we instruct react to use cors and express. It connects to MongoDB, declares the database, gamesCollection and gamesRouter, and listens on a specified port. The app.use is called on '/api/games', gamesRouter this configures the app to use the gamesRouter for the /api/games route.

4. What are the responsibilities of the gamesRouter?
gamesRouter handles the different types of requests, such as fetching all, creating a new game or deleting a game. It decides what action to take based on the type of request (GET, POST, DELETE, etc.)

5. What process does the the client (front-end) use to communicate with the server?
The client (front-end) communicates with requests. In the GamesService.js the client communicates using a fetch. The getGames() sends a GET request. The postGame(payload) sends a POST request and the deleteGame(id) sends a DELETE request.

6. What optional second argument does the fetch method take? And what is it used for in this application? Hint: See Using Fetch on the MDN docs
The second argument is an object that represents additional options to customise the request (e.g. method, body, headers)

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?
The front-end application makes requests to:
GET /api/games to fetch all games.
GET /api/games/:id to fetch a specific game by ID.
POST /api/games to create a new game.
DELETE /api/games/:id to delete a game by ID.
PUT /api/games/:id to update a game by ID.

8. What are we using the MongoDB Driver for?
The driver is used for interacting with the database so that database operations can be completed (CRUD)