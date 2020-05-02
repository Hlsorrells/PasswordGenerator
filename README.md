# PasswordGenerator

## Project Description

  This homework assignment creates a random password generator which generates a password between 8-128 digits based on user-selected criteria.

## Deployment

  [Password Generator](https://hlsorrells.github.io/PasswordGenerator/)

## Table of Contents

  * [Assignment Instructions](#assignment-instructions)
    * [User Story](#user-story)
    * [Acceptance Criteria](#acceptance-criteria)
  * [Project Lessons](#project-lessons)
    * [Creating the bank of characters](#Creating-the-bank-of-characters)
    * [User prompts and responses](#user-prompts-and-responses)
    * [Password Generation Loop](#password-generation-loop)
    * [Error alerts](#error-alerts)
    * [Final assembly and deployment](#final-assembly-and-deployment)
  * [Authors](#author)

----

## Assignment Instructions

Create an application that generates a random password based on user-selected criteria. The complete assignment instructions can be found in the [instruction folder](/instructions). This application will be built in HTML, CSS, and JavaScript to provide a clean user interface and responsiveness to screen size.

  ### User Story

    ```
    AS AN employee with access to sensitive data
    I WANT to randomly generate a password that meets certain criteria
    SO THAT I can create a strong password that provides greater security
    ```

  ### Acceptance Criteria

    ```
    GIVEN I need a new, secure password
    WHEN I click the button to generate a password
    THEN I am presented with a series of prompts for password criteria
    WHEN prompted for password criteria
    THEN I select which criteria to include in the password
    WHEN prompted for the length of the password
    THEN I choose a length of at least 8 characters and no more than 128 characters
    WHEN prompted for character types to include in the password
    THEN I choose lowercase, uppercase, numeric, and/or special characters
    WHEN I answer each prompt
    THEN my input should be validated and at least one character type should be selected
    WHEN all prompts are answered
    THEN a password is generated that matches the selected criteria
    WHEN the password is generated
    THEN the password is either displayed in an alert or written to the page
    ```

## Project Lessons

To begin this project, I roughed out the logic behind the given criteria and the program flow. I constructed some variables to contain user criteria and some if/else statements to manage the conditions. Using a temporary html file named logic as a sandbox, I was able to build and test the code before inserting it into the final script.js file.

### Creating the bank of characters

Construction of the project began with creating the variables to store the user responses and the arrays for all lowercase and uppercase letters, numbers 0-9, and the special characters. 

### User prompts and responses

Variables were created to hold the user response to prompts for selection confirmation of each variable array. Using conditional statements, the arrays selected by the user will be pushed to a new array called "possibles". A partial example of this code was provided by the instructor to demonstrate how to push arrays into a new array.

### Password generation loop

The next step was to construct the for loop creating the password from the available arrays in the "possible" variable. This code was provided by our instructor to demonstrate the use of the Math.floor and Math.random methods which pick a single character from a random array and then assign it to the "result" variable.

### Error alerts

My next task was to create any needed alerts for failed project parameters. Since I created two constraints, I will need to create alerts for each of the constraints.

  #1 No arrays selected
  After completing the four arrays (specials, numbers, lowers, and upppers) to contain the list of character choices, I then began to apply some additional constraints to the project. I needed it to create an alert for the user if no arrays were selected for the password generator. 

  **My First Attempt** This was accomplished by wrapping the for loop for the password generator with an if/else statement. I researched how to determine if an array contained any elements and chose to use the .length property to evaluate whether the "possibles" array was greater than 0 before running the for loop else it would generate an alert indicating that the user needs to select a character type to generate a password. I used console.log(possibles) to verify that the function was operating properly.

  **Final Version** When I was working with the teaching assistant, he showed me how to use the exclamation mark, or bang, as a logical "not" operator in front of the possibles variable within the if statement. This was a much better approach providing the same result.

  #2 Character count outside parameters
  The next step was to create the constraint limiting the length of the password between 8 and 128 characters. Since the user is allowed to enter any number into the prompt, the user's response needed to be validated with a logical test. Using an if statement, passwordLength could be compared to the set parameters of less than 8 or more than 128 which would only pass the alert when either condition was true.

  **My First Attempt** My original approach was to create a single parameter as (8 < passwordLength < 128) but this does not work in JS. I had to seek help from the teaching assistant.

  **Final Version** The teaching assistant showed me that I had to reconstruct the logical argument into two parameters combined with an or operator like so (passwordLength < 8 || passwordLength > 128). This created a return of true if the passwordLength failed project parameters which prompted the alert and the return escape from the function.

### Final assembly and deployment

The final step was to copy the working code from the sandbox logic.html file to the script.js file. The code was inserted into the function generatePassword which I created between the provided variable for retrieving id "generate" and the function writePassword. After final assembly of the script and testing all the parameters, I removed several of the console.log commands for readability and deployed the project on GitHub Pages.

## Author

[Heather Sorrells](mailto:hlsorrells.dev@gmail.com)