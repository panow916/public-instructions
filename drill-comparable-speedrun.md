# Drill - Comparable Speedrun

_(aka Something Compares To You)_

**Accept this project by going here: https://classroom.github.com/a/dRkO6lPv**

## Preamble

A speedrun is meant to practice running through some basic skills as quickly as possible. Unlike non-speedrun drills, where you're typically asked to build a custom class and then "drive" it a bit, a speedrun drill is meant to be done solely in your `public static void main`.

## Time Required

JP's times:

1. importing accepted GitHub repo into Eclipse: **00:42**
2. coding passing solution: **10:23**
3. punting solution back to GitHub repo: **00:43**
4. submitting and verifying result: **01:19**

Your target time for step 2: **42 minutes**

## Skills Covered

Show you can...

- [ ] implement Comparable<T>.
- [ ] initialize an array with shorthand/shortcut syntax.
- [ ] use `compareTo` in a conditional.

## Instructions

1. Each of `Material`, `Movie`, and `NoiseReading` needs to implement `Comparable` - read the note about the natural ordering for each class in the class documentation and then implement `Comparable` for each class.
2. Complete the **//TODO** entries in the `main` method in the `Main` class provided, using the documentation to guide you.
   1. **Don't forget to complete the one in the `position` method!**
   2. If you have completed the tasks in (1) and (2) properly, you will pass all the tests in `MainTests`.
   3. You might find it useful to run your main if your tests aren't passing. Here is an example of a correctly working main (user input in **bold**):

---
---

Noise reading in dB? **120**  


Here are the natural orderings for the 3 NoiseReading objects in the Comparable[] array:   
12dB @ (41.6,144.5) is the same as 12dB @ (41.6,144.5)  
12dB @ (41.6,144.5) comes after 120dB @ (41.6,-32.4)  
12dB @ (41.6,144.5) is the same as 12dB @ (41.6,-154.4)  
120dB @ (41.6,-32.4) comes before 12dB @ (41.6,144.5)  
120dB @ (41.6,-32.4) is the same as 120dB @ (41.6,-32.4)  
120dB @ (41.6,-32.4) comes before 12dB @ (41.6,-154.4)  
12dB @ (41.6,-154.4) is the same as 12dB @ (41.6,144.5)  
12dB @ (41.6,-154.4) comes after 120dB @ (41.6,-32.4)  
12dB @ (41.6,-154.4) is the same as 12dB @ (41.6,-154.4)   

Name of material? **milk**  

Denisty of material? **1027**  


Here are the natural orderings for the 3 Material objects in the Comparable[] array:  
milk(1027.00kg/m3) is the same as milk(1027.00kg/m3)  
milk(1027.00kg/m3) comes after blood(1.60kg/m3)  
milk(1027.00kg/m3) comes before granite(2700.00kg/m3)  
blood(1.60kg/m3) comes before milk(1027.00kg/m3)  
blood(1.60kg/m3) is the same as blood(1.60kg/m3)  
blood(1.60kg/m3) comes before granite(2700.00kg/m3)  
granite(2700.00kg/m3) comes after milk(1027.00kg/m3)  
granite(2700.00kg/m3) comes after blood(1.60kg/m3)  
granite(2700.00kg/m3) is the same as granite(2700.00kg/m3)  

Title of movie? **The Excorcist**  

Year of release? **1973**  


Here are the natural orderings for the 3 Movie objects in the Comparable[] array:  
Aliens (1986) is the same as Aliens (1986)  
Aliens (1986) comes after Battleship Potemkin (1925)  
Aliens (1986) comes after The Excorcist (1973)  
Battleship Potemkin (1925) comes before Aliens (1986)  
Battleship Potemkin (1925) is the same as Battleship Potemkin (1925)  
Battleship Potemkin (1925) comes before The Excorcist (1973)  
The Excorcist (1973) comes before Aliens (1986)  
The Excorcist (1973) comes after Battleship Potemkin (1925)  
The Excorcist (1973) is the same as The Excorcist (1973)  

---
---

> **Careful!**
> - read the natural ordering information of each class carefully
> - `Movie` uses the `Year` class...which in Java already implements Comparable...you should use this to your advantage!
> - you should use the `Double.compare` method to handle implementing a proper compareTo that involves doubles
> - when you initialize the arrays in `main`, make sure you make them the specified type....


## Tests

> *Since this is the first week of drills, I'll explain in detail what's going on with testing. After the first week, I'll assume you're cool with it.*
Your code is being tested through `MainTests.java`. Although it looks kinda scary, all that's going on is this:

1. The test is told what things to "type" when prompted by your `main` code. For example, in the "Bronco Billy" test, the things "typed" will be: **15**, **aluminium**, **2700**, **Stand By Me**, and **1986** - in that order.
2. The test then runs the main, "typing" its input and observing what comes out in the console. That output is checked line-by-line with the Strings you see in the `List.of` part of the test. Your output has to match these Strings **exactly** - the order, spelling, and even capitalization all have to match for the test to pass. Using the `Compare Actual With Expected Test Result` mini-button is a **lifesaver** here!