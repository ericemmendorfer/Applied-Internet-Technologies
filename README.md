# Applied-Internet-Technologies  CSCI-UA467 
Taught by Joseph Versoza  

Homework and projects from Applied Internet Technologies course Spring 2024

### Homework 1: Crazy 8's
<details>
<summary>Overview:</summary>  
Description
  <br>
Create a demo of an interactive card game, Crazy Eights, that allows two turns to be played (one "player" turn and one computer turn).

<li> the game will use a standard 52-card deck of French suited playing cards
</li> <li> a configuration file will be used to set the cards remaining the in the draw pile, the player's hand and the computer's hand
</li> <li> alternatively, without a configuration, the game will generate a deck of cards, shuffle, and deal five cards to each player
</li> <li> a single card is drawn from the draw pile - it is used as the starter
</li> <li> the starter card dictates the suit or rank that should be played next
</li> <li> for example, if the starter is 2♦️
</li> <li> …then the next card to played must have either a rank of 2 or a suit of ♦️
</li> <li> the player and computer alternate turns discarding a single card from their hand that matches either the suit or rank of the starter
</li> <li> a card with a rank of 8 can be placed at any time regardless of the rank and suit of the starter
</li> <li> if an 8 is played, then the suit of the starter can be set
</li> <li> for example, if the starter is 2♦️
</li> <li> …and an 8 is played
</li> <li> the suit can be set to any of the four suits: ♠️ ❤️'♣️ ♦️
</li> <li> if a card cannot be played, cards must be drawn from the draw pile until a card can be played (otherwise pass)
</li> <li> the first to discard all of the cards in their hand wins!
</li> <li> 👀 Note however that the demo will only have two turns: the player first, and the computer second. The computer's turn logic will be limited. </li>
<br>
You'll create this game in 2 parts:

<li>create functions for managing a standard 52-card deck (you may use these functions in the next part, but you are not required to do so)  </li>
<li>create an interactive demo of the first two turns of a game of Crazy Eights</li>
<br>
<details>
<summary>Objectives:</summary>  
<li>Write some JavaScript!</li>
  <li>control structures  </li>
 <li> functions  </li>
 <li> Object, Array, and string manipulation  </li>
 <li> Learn how to run node programs  </li>
  <li> Learn about node built-ins:  </li>
 <li> process  </li>
  <li>the fs module  </li>
 <li> import and export  </li>
 <li> Install and use ES Modules; create your own  </li>
 <li> Run unit tests to check your work  </li>
<li>  Use a static analysis tool (eslint) to help prevent bugs / errors </li>
</details>
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Homework 2: Higher Order Functions, Classes, Net Module
  
<details>
<summary>Overview:</summary>  
Description  
 <li> hoffy.mjs - write a series of functions that demonstrate the use of the rest operator (or call/apply), and higher order functions  </li>
 <li> drawing.mjs - create a class that represents svg markup  </li>
 <li> sfmovie.mjs and report.mjs - create functions and a short program to read data from a file and analyze that data using map, reduce, and filter  </li>
</details>

Code Submitted  
Grade    
Reasoning    
Code Corrected

### Homework 3: A Web Server for Static Files
<details>
<summary>Overview:</summary>  
Description: <br> 
Create a web server that:
<br>
  
<li> allows "redirect" configuration  </li>
<li> serves static files such as html files, images, and css… from a specific directory  </li>
<li> serves markdown files as compiled html  </li>
<li> displays list of links to contained files and directories if the url path is directory  </li>
<li> At the end, you'll have a toy http server that you can use to serve files and directory indexes.</li>
  <br>
Again, this web server will be built off of and run from node's built-in TCP server (from the net module).
  
You can only use the following modules for this assignment →
  
<li>net - for creating TCP servers and clients  </li>
<li>fs - a module for file system related tasks, such as reading and writing files  </li>
<li>path - a module for file name and path related manipulation (such as extracting an extension from a file name and joining path names)  </li>
<li>url - to convert a file url to a file path  </li>
<li>markdown-it - a module for compiling markdown into html (must be installed)  </li>
⚠️You can't use the http module… or install additional web related libraries, such as express  
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Homework 4: Kaomoji Texting
<details>
<summary>Overview:</summary>  
Description  
Create a site that takes a text message and replaces the words representing emotions with kaomoji! <br>
E.g. "Today's weather is nice and it makes me happy" -> "Today's weather is nice and it makes me ♥(ˆ⌣ˆԅ)"
  <br>
Kaomoji is a Japanese version of emoticons (such as :) for a smiling face). They tend to be more expressive than traditional emoticons, hence more fun to play with.
  <br>
Additionally, users will be able to manage the mapping of words with kaomoji through the manipulation of an in-memory data store.
  <br>
In this homework you'll be working with:
  
<li>serving static files  </li>
<li>middleware  </li>
<li>handling and creating forms: GET and POST  </li>
<li>storing and managing data in-memory  </li>
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Homework 5: More Colors / Let's Watch Some Movies! (Sessions and Storing Data)
<details>
<summary>Overview:</summary>  
Goals:
<br>
There are two main parts to this assignment:
<br>
Session Management / Handling Cookies (Part 1)  
<li>build your own middleware to parse cookies  </li>
<li>build your own middleware to create an in-memory session store  </li>
Storing and Retrieving Data (Parts 2 - 6)  
<li>use the commandline mongodb client to create a database, collection and several documents  </li>
<li>use mongoose to read data from mongodb  </li>
<li>use mongoose to write data to mongodb  </li>
<li>use pre-built session middleware (Part 6)  </li>
  <br>
Description  <br>
By the end of this project… you should be familiar with:
  
<li>writing middleware  </li>
<li>setting and reading cookies  </li>
<li>some basic read and write operations with mongodb…  </li>
<li>integrating mongodb with an Express web application using Mongoose </li>
<br>
You'll create / modify two express apps:    
A simple demo site that has two pages (partially written for you):  <br>
a page to change the background color of the site: /preferences  
<li>has a simple form   </li>
<li>changes made in the form are stored in the user's session   </li>
<li>a page showing the current data that's stored in that user's session: /  </li>
<br>
A site that has a list of movies:  
<li>the first page is a list of movies: /movies  </li>
<li>displays a table of movies  </li>
<li>has a form to filter the movies by director name  </li>
<li>the second page allows the user to add movies: /movies/add </li>
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Homework 6: Authentication and One Hand of Blackjack (Client Side JavaScript)
<details>
<summary>Overview:</summary>  
Description  <br>
Login, Registration, and Multiple Models  <br>
Finish a link aggregator site (like reddit, hacker news, etc.) that supports user registration and login… along with the ability to post articles (links).
  <br>
Registering or logging in will create an authenticated session that contains all of the logged in user's information. Some elements on pages will only appear when a user is logged in. Some pages will redirect to login if a user arrives unauthenticated.
    <br>

Most of the code for this is already written; only three functions must be implemented
    <br>

Goals  
<li> use bcrypt.js (argon2 is suggested by owasp, but argon2 may not install on all systems) to salt and hash a password and to compare a hash to a plain text password  </li>
<li>use the slides on authentication to implement login and registration  </li>
<li>use req.params to capture a part of the url path  </li>
<br>
The starter code also contains:
  
<li>express-session to store user data / an authenticated session  </li>
<li>referenced documents to model users and posted articles  </li>
⚠️⚠️⚠️ WARNING ⚠️⚠️⚠️  
This homework is for learning purposes only; do not use it for authentication on a deployed site
  <br>
our application will only be served locally, and consequently, it will not be served over an encrypted connection … and - related - cookies aren't set to secure  
<li>it will allow case sensitive usernames  </li>
<li>not all errors are accounted for or handled gracefully  </li>
<li>system level errors and user errors may not be distinguishable  </li>
<li>some error messaging may reveal too much information  </li>
<li>user interaction and error messaging will be minimal (for example, successful login should redirect to page that required login)  </li>
<li>some error messages reveal info about the existence of a user  </li>
<li>our secret for session options is kept in our repository  </li>
  <br>
Features:  
<br>
The following features are partially implemented
  
<li> register a new account  </li>
<li> login using an existing account  </li>
<li> show a single article's details  </li>
<br>
These features are fully implemented:
  
<li>view all posted articles  </li>
<li>add a new article (only when logged in)  </li>
<li>prevent / allow access to certain ui elements or pages based on authenticated status  </li>
<br>
The app has 5 pages and 3 forms: 
<li>/ - lists all articles  </li>
<li>/register - register form  </li>
<li>/login - login form  </li>
<li>/article/add - add new article form  </li>
<li>/article/:slug - detail page for a specific article </li>
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Homework 7: Anonymous Q&AIT (AJAX)
<details>
<summary>Overview:</summary>  
Goals / Topics Covered:
  <br> 
  
  You'll be using the following concepts:
<li>fetch</li>
<li>sending back json from Express  </li>
<br>
Description  
  <br>
Create a question-and-answer site where users post questions and answers to these questions anonymously. You will create this "single page app" using AJAX calls instead of regular page rendering and form submission.  
<br>
<br>
You will:  
<li> Implement routes to create an API for retrieving questions and adding new ones  </li>
<li>Use JavaScript to trigger background requests to the API from the form submit buttons</li>
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected

### Final Project (AteIt)
<details>
<summary>Overview:</summary>  
</details>

Code Submitted  
Grade  
 Reasoning  
Code Corrected
