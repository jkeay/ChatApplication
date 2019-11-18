# Full Stack Chat Application

## Overview
The project consists of a Full Stack solution to creating a chat application. Our application utilizes a NodeJS server to build the web pages which the client requests. The formats in the project include: .pug, .scss, and .js (ES6)

## Conversions
### Pug
Pug is a templating format which includes a NodeJS module for preprocessing .pug files into .html.
The templates are stored on the server and no .html files ever exist on the server-side other than the temporary creation of an index.html sent to the client.
> Preprocessor: pug - tasked to retrieve .pug files and gather requirements before rendering

### ES6
ES6 is a common standard for JavaScript which is not fully supported on all browsers.
Most of our code is server side and running through NodeJS and by default reads ES6 format.

### SCSS
SCSS is a "sassy" form of css which allows for many of the features in CSS3 and still convert to lower format of CSS for all browsers.
Unlike the templating solution with .pug files, .css files are requested in the .pug template files and must be physically generated.
> Preprocessor: node-sass-middleware - tasked to retrieve .scss files, gather requirements, and sending a converted .css file

## Chat application
### Flow
A client who first accesses the chat application will be prompted with a login screen.
Our login/user creation extends off of our tech-eval project and utilizes [Firebase](https://firebase.google.com/) for managing our database of users.
In order to view / use the chat application a client must have a user account and be logged in, or else Express will redirect the client to the login page.

### Testing
The express application is set to run on port:3000 so after running vagrant up you can access the application at [localhost:3000](localhost:3000).
You can then either create a new user and include
#### Required Fields
- Username
- Name
- Password (& Confirm Password)  

(or) you can login with an existing user:
> Username: TestUser  
> Password: Password1

The main window of the chat allows users to submit messages between other logged-in users.
A side bar displays all the logged in users for the chat application by the server keeping track of sign-in and log-out events.
> User sessions are stored in a browser cookie, so as long as the browser is still open the user will be logged in

## Demonstration Pages
Three pages have been included to help present to students how each of the three standards compare to HTML, CSS, and native JavaScript. All examples include real comparisons with code used to run the chat application and the equivalent code performed in a native format.
