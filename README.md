# PasswordGenerator
This homework assignment creates a random password generator which creates a password between 8-128 digits based on user-selected criteria.

# Assignment Instructions
Create an application that generates a random password based on user-selected criteria. The complete assignment instructions can be found in the [instruction folder](/instructions). This application will be built in HTML, CSS, and JavaScript to provide a clean user interface and responsiveness to screen size.

# Project Lessons
To begin this project, I roughed out the logic behind the given criteria and the program flow. I constructed some variables to contain user criteria and some if/else statements to manage the conditions. These logical statements are written within the script tag in the index.html file.

Construction of the project began with creating the variables to store the user responses and the arrays for all lowercase and uppercase letters, numbers 0-9, and the special characters. These arrays will be pushed to a new array called "possibles" using conditional statements to contain all arrays selected by the user. The variable "possibles" and "results" are defined but not assigned resulting in two empty arrays/sets. A partial example of this code was provided by the instructor to demonstrate how to push arrays into a new array.

The next step was to construct the for loop creating the password from the available arrays in the "possible" variable. This code was provided by our instructor to demonstrate the use of the Math.floor and Math.random methods which pick a single character from a random array and then assign it to the "result" variable.

After completing the four arrays (specials, numbers, lowers, and upppers) to contain the list of character choices, I then began to apply some additional constraints to the project. I needed it to create an alert for the user if no arrays were selected for the password generator. This was accomplished by wrapping the for loop for the password generator with an if/else statement. I researched how to determine if an array contained any elements and chose to use the .length property to evaluate whether the "possibles" array was greater than 0 before running the for loop else it would generate an alert indicating that the user needs to select a character type to generate a password. I used console.log(possibles) to verify that the function was operating properly.

My next step is to make sure that the password generated includes a character from each array.