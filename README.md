# COP2664-1-Lesson-3-Programming-Exercise-3-2
This is a GitHub repository link for Programming Exercise 3-2 of Lesson 3.

// This program is used to determine the price of a movie ticket based on the age of the customer and what time of day it is whether the movie starts at daytime or nighttime.

let timeOfDay = "night" // or "day"

let age = 25 // or any other age

var ticketPrice: Double = 0.0 
switch timeOfDay.lowercased() {
  // day time price is $8 for everyone age 4 or higher
case "day":
    if age >= 4 {
        ticketPrice = 8.00
    } else {
        ticketPrice = 0.0 // free for anyone under age 4
    }
case "night":
   // nighttime price based on age ranges
   switch age {
   case 4...16:
      ticketPrice = 12.0
   case 17...54:
      ticketPrice = 15.0
   case _ where age >= 55:
      ticketPrice = 13.0
   default:
      ticketPrice = 0.0 // free for anyone under age 4
}
default:
   print("Invalid time of day entered.")
   ticketPrice = -1.0 // invalid time input
}
if age >= 4 && age <= 16 { // children age 4 to 16
    ticketPrice = 12.0 // children ticket price
} else if age >= 17 && age <= 54 { // adult age 17 to 54
    ticketPrice = 15.0 // adult ticket price
} else if age >= 55 { // senior age 55 and above
    ticketPrice = 13.0 // senior ticket price
} else {
    ticketPrice = 0.0 // invalid age
}
print("The ticket price is $\(ticketPrice)" ) // output the ticket price
