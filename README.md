# CS360-Mobile-App.-Development

***Briefly summarize the requirements and goals of the app you developed. What user needs was this app designed to address?***
The user required an application that will be used to track items in a warehouse. They required the application to include the following:
A database with at least two tables (one to store the inventory items and one to store user logins and passwords),
a screen for logging into the app (Note that this should also be used to create a login if the user has never logged in before.),
a screen with a grid that displays all items in the inventory,
a mechanism by which the user can add and remove items from inventory,
a mechanism by which the user can increase or decrease the number of a specific item in the inventory,
and a mechanism by which the application will notify the user when the amount of any item in the inventory has been reduced to 0 (zero).

***What screens and features were necessary to support user needs and produce a user-centered UI for the app? How did your UI designs keep users in mind? Why were your designs successful?***
The user required a feature to support a user logging into the application. This required the need for a login/register screen so users could be authenticated and authorized. The screen met the user’s requirements by including the following:
Fields for the user to provide a username and password
The password element was configured in a way that obscures any text that is typed into the field. 
A button for the user to submit their username and password
A button for the user to create a new login if it is their first time using the application.

The user also required a data display screen for showing all items being tracked in the application. This screen had to include:
A grid for displaying data
Logical labels and headers for the data that will be displayed
A button for adding data to the grid
A button on each row for deleting that row of data from the grid
A mechanism that allows a user to change the value associated with each grid item (e.g. the number of a specific item in an inventory or the date of an event)

Lastly, the user requested a screen that included a button which would ask the user for permissions to send an SMS message when the inventory count of an item was 0. User denial of this permission would not interfere with the functionality of the application.

***How did you approach the process of coding your app? What techniques or strategies did you use? How could those be applied in the future?***
I approach developing applications from an incremental and iterative perspective when appropriate. I usually prefer to work on small chunks of code at a time, test what can be tested, and move onto the next phase. I also like to iterate upon segments of my software to where I gradually enhance parts of the application as I revisit them once they have already become usable but unrefined in some perspectives. I apply regression testing as I develop to make sure newer code doesn’t negatively affect the previous code.  

***How did you test to ensure your code was functional? Why is this process important and what did it reveal?***
Much of my development revolves around testing. I apply the 5 Software Testing Techniques where applicable. 

As stated previously, I use Static Testing to avoid potential problems in the future. In this situation, this revolved around analyzing the UI for its compatibility with the features I wanted to include and program such as a ListView with button functionality for each row. 

I used Unit Testing to test specific parts of the code. This ranged from providing conditional statements to outputting values to the console for data analyzation. An example of this was identifying the size of my ArrayList containing my Items during onCreate(), onStart(), and onStop(). 

I used Integration Testing to depict if my imported classes and all my screens were working together as intended. This was done by running and navigating through parts of the program that used multiple classes/components such as the Inventory Screen and making sure my adapter class, database class, activity class, UI and imports were all operational and operating correctly when running simultaneously. 

I utilized System Testing by handing my software off to my professor and fiance (thank you both!) and gathered their evaluations of the software. My fiance was especially helpful in providing “constructive” comments on the UI. 

Because we technically didn’t have a “client”, my form of Acceptance Testing was then running the program as a whole and making sure it met each of the requirements as specified in the guidelines/rubric. The professor’s evaluation of the software and release of feedback will also serve as a form of Acceptance Testing.

***Considering the full app design and development process, from initial planning to finalization, where did you have to innovate to overcome a challenge?***
I had to innovate during several sections of this application although I assured that these innovations still were within user needs. One was that the ArrayLists used to store items involving the adapter would persist so items were duplicated on the view. I resolved this by making use of the onStart() and onStop() feature to reset each of these components to avoid duplicates. I also faced an issue with performance during the end of my SDLC. I then went back and provided background threads to all database-related commands so the main thread was not being overworked and made the project to where it can handle many objects. A final obstacle where I had to innovate that I will divulge is how items were formatted on the UI. I found that if users input a very large name and/or count that formatting would get messy even with pagination included. Therefore, I set limits on user input to reasonable extents such as not letting the count of an item be greater than or equal to a billion.

***In what specific component from your mobile app were you particularly successful in demonstrating your knowledge, skills, and experience?***
I worked hard on this project and feel I was successful in several areas. However, I believe I was particularly successful at handling the coding/data flow involving database classes. I used a SQLite Database and applied proper techniques using CRUD operations involving the data. I also added checks into these database classes such as seeing if an item’s name would be duplicated in the database or if a username already existed in the database.
