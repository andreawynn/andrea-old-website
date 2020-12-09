## Automated Dataset Generator for Machine Learning Systems
## Course: CSSE490 - Software Engineering for Machine Learning
*Completed in Fall 2020-21*

**Please note that I cannot share the source code or files for this course project due to academic integrity regulations at Rose-Hulman.**

### Motivation for Project
The motivation for the project comes from the real-world issue of getting good training datasets in the field of machine learning. Typically, unless a specific dataset you need to use for training a ML model happens to be publicly available, you will need to spend a lot of human time, energy, and potentially other resources to create, sort, and/or label your own dataset. 

But... What if we had access to an enormous dataset containing pretty much everything you could think of, that was already human-labeled and is being updated in real-time?

The answer: We do! Many posts (including both text and images) on social media sites such as Twitter, Instagram, and Facebook come pre-labeled with user-defined hashtags, which are essentially a way for users to indicate what their particular post is related to. These hashtags could then be used to create a labeled dataset to help train ML models. This is the idea upon which the dataset generator project was built.  

### Project Description
The dataset generator project features an innovative filtering algorithm that takes in data in real-time from Twitter, selects posts that are relevant to a keyword entered by the user, and writes those posts (along with convenient labels for training ML systems) out to a file, which can then be used as a dataset for training and validating Machine Learning systems. 

The generator works by first asking the user for a set of "starting" hashtags, or labels, that describe the subject they would like to capture within the dataset. For example, if the user enters the word "dog", the system will search for the specified number of tweets with the hashtag "dog", and will select the relevant hashtags from each post to serve as the labels for each dataset entry. 

The system uses an innovative hashtag filtering algorithm, developed by me and my partner during this project, which considers factors such as how often certain hashtag pairs appear together and whether a user marks hashtags as "irrelevant" to determine whether a specific hashtag should be included as a label for a certain post. In this way, each dataset entry only retains the relevant labels, and the others are discarded. 

My team received a high A on this project for meeting and exceeding all milestone deadlines and requirements, and even earned some extra credit for the innovative idea and algorithm upon which this system was based. 

### Project Demo
To see a live demo of the project, please watch the video here: https://youtu.be/REwsMd0hNe8

### My Contribution
I worked on nearly all aspects of this project, along with my partner. 

Near the beginning of the project, and throughout the project as well, I worked with my partner to develop and test the system with representative users. I also worked with my partner to develop the hashtag filtering algorithm, as well as the structure of the project itself. 

I wrote the hashtag filtering algorithm, including additional functionality which allows the specific state of the hashtag filter's "learning" so that it can be exactly replicated on different machines. 

I also wrote a significant portion of the user interface using Tkinter, including the basic interface for all pages, the connectivity with the Twitter data fetching and hashtag filtering code, and handling the collection and implementation of user feedback in the hashtag filtering algorithm. 

### Technical Architecture and Tools Used
*Programming Languages* <br>
Python - This entire project was coded in Python. The graphical user interface was implemented using Tkinter, a package developed for Python. <br>

*APIs* <br>
Twitter API - My team used the Twitter API to fetch data directly from Twitter, as well as to fetch hashtags for each post. 

*Version Control* <br>
GitHub - I used GitHub to collaborate with my teammate for this project and ensure that our work was up to date.

*Editing Tools & Environments* <br>
JetBrains PyCharm - I used PyCharm for coding in Python throughout this project. 
