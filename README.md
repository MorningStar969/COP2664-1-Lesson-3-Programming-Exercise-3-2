# COP2664-1-Lesson-3-Programming-Exercise-3-2
This is a GitHub repository link for Programming Exercise 3.2 of Lesson 3.

// This program is used to determine the price of a movie ticket based on the age of the customer and what time of day it is whether the movie starts at daytime or nighttime.

let timeOfDay = "night" // or "day"

let age = 60 // or any other age

var ticketPrice: Double = 0.0 // or any other price

switch timeOfDay.lowercased() { // or .uppercased()
   case "day": // or "night"
       if age < 4 { // or any other age
           ticketPrice = 0.0 // or any other price
       } else { // or any other age
           ticketPrice = 8.0 // or any other price
       }
   case "night": // or "day"
       if age < 4 { // if age is less than 4
           ticketPrice = 0.0 // it will be free
       } else if age >= 4 && age <= 16 { // if age is between 4 and 16
           ticketPrice = 12.0 // it will be $12
       } else if age >= 17 && age <= 54 { // if age is between 17 and 54
           ticketPrice = 15.0 // it will be $15
       } else { // if age is greater than 54
           ticketPrice = 13.0 // it will be $13
       }
   default: // if timeOfDay is not "day" or "night"
       print("Invalid entry") // it will print "Invalid entry"
}
print("The ticket price is $\(ticketPrice)") // it will print the ticket price
