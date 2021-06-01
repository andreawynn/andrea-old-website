## Game Recommendations Database Project
## Course: CSSE433 - Advanced Database Systems
*Completed in Spring 2020-21*

**Please note that I cannot share the source code or files for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The goal of this project was to recommend games to users based on the games they already like by referencing existing Steam game reviews. Users may create and log in to their own accounts to access the recommendation platform, view a game's description and recent reviews of the game, and create new reviews for games. Users can also choose to receive a curated list of game recommendations based on a list of games that they previously enjoyed. 

This project utilizes 3 different NoSQL databases - OrientDB (graph database), MongoDB (document-based database), and REDIS (key-value in-memory database). It handles horizontal scalability through sharding, replication, replica sets with primary/secondary nodes, and other strategies discussed in more detail in the document linked below. Additionally, Apache Kafka is used to handle sending requests to all nodes of the databases. Because this is an application designed to be inherently scalable (even our initial dataset of Steam reviews was tens of gigabytes in size), horizontal scalability and maintaining data consistently across multiple nodes was a major concern throughout the project. 

The full description of scalability and consistency across all 3 databases can be found here: https://docs.google.com/document/d/13s_yY4_DinEIvvSHKSg5dGWJcTODIYX1_CP-nFNyt0Q/edit?usp=sharing

### My Contribution
For this project, I designed the schema for all three NoSQL databases (database schemas pictured at bottom of page). I optimized the schemas for specific common and important query types that would be performed on each database, such as generating recommendations for a user by taking advantage of OrientDB's graph structure and efficient pattern matching queries and storing larger and more complex data structures such as detailed review or game information in MongoDB. Additionally, I worked to reduce data duplication across databases; for example, when storing information about users and the games they recommended and didn't recommend in OrientDB, users and games are only referred to by their unique ID and do not store any additional information not needed for the recommendation queries. 

Additionally, I wrote the MongoDB backend connection with NodeJS. Specifically, I implented functions such as retrieving information about specific users and games; getting all games with positive reviews from a user; listing all games and users in the system; pulling information from games and users to display on screen; etc. This code served as the interface between the application and the databases used for the project. 

I also handled all data importing from an Excel spreadsheet (containing over 10 GB of data) into the databases, according to the specified schema. I wrote a script in Python, using PyMongo to connect to the MongoDB instance, and another script in Javascript, using OrientJS to connect to the OrientDB instance, to import data from the spreadsheet into those databases. In both scripts, I dealt with handling arbitrarily large files, checking rows for valid CSV formatting and data types, handling missing values, and not inserting duplicate information. 

Additionally, I set up the MongoDB instance, including running multiple nodes on different machines and putting them together in shards and clusters. 

### Technical Architecture and Tools Used
*Programming Languages and Frameworks* <br>
NodeJS - The application back end was implemented in NodeJS. Our team chose to use NodeJS because it interfaces well with all three databases used in the project. <br>
HTML/CSS/Javascript - These were used to implement the front end user interface for the application, and connected to the NodeJS back end to display the user interface for all features described above. <br>

*Databases and Distributed Technologies* <br>
OrientDB Graph Database - Used for associating a specific reviewer with their rating for a game (recommended vs not recommended). This enables quick access to the rating that a particular user gave for a particular game. <nr>
MongoDB Document-Based Database - Used to store information about each review and each game. This enables all information about a specific review, as well as all information about a specific game, to be quickly accessed. <br>
REDIS Key-Value, In-Memory Database - Used to store the user IDs and their corresponding passwords and selected language (if applicable) for a particular session of this application. This allows for very fast access to user data, and any new reviews written by users will be written back to MongoDB once the review has been written. <br>
Apache Kafka Distributed Messaging Framework - Used to communicate reliably between the application and all nodes of the databases. 

### Database Schemas
Following are the data schemas used within the 3 databases: OrientDB, MongoDB and REDIS. 
  
OrientDB data schema: <br> 
  <img src="../images/orientdb_model.png?raw=true" height="300" width="auto"/> <br>
MongoDB data schema (users): <br>
  <img src="../images/mongodb_review_model.png?raw=true" height="300" width="auto"/> <br>
MongoDB data schema (games): <br>
  <img src="../images/mongodb_game_model.png?raw=true" height="300" width="auto"/> <br>
REDIS data schema: <br>
  <img src="../images/redis_model.PNG?raw=true" height="300" width="auto"/> 
