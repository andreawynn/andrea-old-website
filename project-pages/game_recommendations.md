## Game Recommendations Database Project
## Course: CSSE433 - Advanced Database Systems
*Completed in Spring 2020-21*

**Please note that I cannot share the source code or files for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The goal of this project was to recommend games to users based on the games they already like by referencing existing Steam game reviews. Users may create and log in to their own accounts to access the recommendation platform, view a game's description and recent reviews of the game, and create new reviews for games. Users can also choose to receive a curated list of game recommendations based on a list of games that they previously enjoyed. 

This project utilizes 3 different NoSQL databases - OrientDB (graph database), MongoDB (document-based database), and REDIS (key-value in-memory database). It handles horizontal scalability through sharding, replication, replica sets with primary/secondary nodes, and other strategies discussed in more detail in the document linked below. Additionally, Apache Kafka is used to handle sending requests to all nodes of the databases. Because this is an application designed to be inherently scalable (even our initial dataset of Steam reviews was tens of gigabytes in size), horizontal scalability and maintaining data consistently across multiple nodes was a major concern throughout the project. 

The full description of scalability and consistency across all 3 databases can be found here: https://docs.google.com/document/d/13s_yY4_DinEIvvSHKSg5dGWJcTODIYX1_CP-nFNyt0Q/edit?usp=sharing

### My Contribution
**TODO** edit this section

I worked primarily on the SQL server back-end for this project, but I also wrote some of the webpages and helped implement a significant portion of the connectivity between the website and SQL server. 

For the SQL back-end, I designed the relational schema and implemented the majority of the stored procedures (including those for hashing and salting user passwords before storing them in the database; writing, editing, and deleting notes and pages; accessing books, notes, and pages; and creating bookmarks, among many others). For all my stored procedures, and some of my teammates' as well, I also implemented parameter validation and user permission checking. 

On the website, I created the interface for viewing all books in a user's library; viewing pages; writing notes; adding bookmarks; and creating new books. I also worked with one of my teammates on getting user registration and login set up, and I worked with my team to help ensure that the website front-end was connected properly and was appropriately interacting with the SQL server back-end. 

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
  
  
