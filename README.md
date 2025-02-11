# COP2664-1-Lesson-3-Programming-Exercise-3-2
This is a GitHub repository link for Programming Exercise 3-2 of Lesson 3.

// This program is used to calculate the price of a movie ticked based on the age of the customer and the time the movie is playing.

import Foundation // Imports the Foundation library
print("Enter 'day' or 'night': ") // Prints the string "Enter 'day' or 'night': "
var time = readLine() // Declares a variable named time and assigns it the value of the user input
print("Enter your age: ") // Prints the string "Enter your age: "
var age = Int(readLine()!)! // Declares a variable named age and assigns it the value of the user input
switch (time, age) { // Starts a switch statement with the variables time and age as the cases
  case ("day", _): // If the variables time and age are equal to the case, the following code will run
    print("Your ticket price is $8") // Prints the string "Your ticket price is $8"
  case ("night", _): // If the variables time and age are equal to the case, the following code will run
    print("Your ticket price is $12") // Prints the string "Your ticket price is $12"
  case ("night", 4...17): // If the variables time and age are equal to the case, the following code will run
    print("Your ticket price is $15") // Prints the string "Your ticket price is $15"
  case ("night", 18...55): // If the variables time and age are equal to the case, the following code will run
    print("Your ticket price is $13") // Prints the string "Your ticket price is $13"
  case ("night", _): // If the variables time and age are equal to the case, the following code will run
    print("Your ticket price is $12") // Prints the string "Your ticket price is $12"
  default:
    print("Your ticket price is $0") // Prints the string "Your ticket price is $0"
}
