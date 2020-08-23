## A* Map Navigation Project
## Course: CSSE230 - Data Structures & Algorithm Analysis
*Completed in Winter 2018-19*

**Please note that I cannot share the source code or files for this course project due to academic integrity regulations at Rose-Hulman.**

### Project Description
The Choose Your Own Adventure Database Project features a simple website interface coupled with a SQL database back-end that provides a scalable digital solution for Choose-Your-Own-Adventure style novels. It features secure user registration and login with password hashing and salting, as well as other security features such as parameter validation. 

When a user creates an account and logs in, they may view a list of CYOA-style novels that are available in the database. Each of these novels tracks the user's progress by saving the user's previously visited pages and current page, and also allows the user to create their own bookmarks or write notes associated with certain pages (all of which are stored in the database and thus preserved between sessions). The user cannot view pages they have not seen yet, to prevent potential spoilers for later in the story; if a user tries to access a new page indirectly by modifying the page number in the website address bar, they are redirected to an error page and returned to the main menu. 

The system also provides support for authors to write or upload existing books to the database, which then become accessible to other users. Any user may create a new book, which can be made accessible to all users as readers, but only users authorized by the book's creator may edit the book. The webpage interface provides full support for writing books, including creating the book, writing individual pages, linking pages, and deleting pages. The project also features a Python script for importing data from an unsorted Excel spreadsheet into the SQL database server according to the relational schema for the database, which is another way to add books to the database from the back-end. 

Our team received a high A on this project for meeting and exceeding all milestone deadlines and requirements, and even earned some extra credit for implementing additional features such as user registration and data importing. 

### My Contribution
I worked primarily on the SQL server back-end for this project, but I also wrote some of the webpages and helped implement a significant portion of the connectivity between the website and SQL server. 

For the SQL back-end, I designed the relational schema and implemented the majority of the stored procedures (including those for hashing and salting user passwords before storing them in the database; writing, editing, and deleting notes and pages; accessing books, notes, and pages; and creating bookmarks, among many others). For all my stored procedures, and some of my teammates' as well, I also implemented parameter validation and user permission checking. 

On the website, I created the interface for viewing all books in a user's library; viewing pages; writing notes; adding bookmarks; and creating new books. I also worked with one of my teammates on getting user registration and login set up, and I worked with my team to help ensure that the website front-end was connected properly and was appropriately interacting with the SQL server back-end. 

### Technical Architecture and Tools Used
*Programming Languages* <br>
SQL - The back-end database for this project was implemented entirely in SQL, per project requirements. 
JavaScript - Our team chose to use JavaScript for the website. 
HTML - Our team chose to use HTML to design the webpage interface for this project. 

*Version Control* <br>
GitHub - I used GitHub to collaborate with my two other teammates for this project and ensure that our work was up to date.

*Editing Tools & Environments* <br>
Microsoft SQL Server Management Studio - I used SQL Management Studio for coding in SQL and managing the back-end database. 
Notepad++ - I chose the Notepad++ editor for the Javascript/HTML portions of this project. 
