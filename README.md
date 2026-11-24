# JoshPocketEdition
Recovery Flight Computer coding repository. 

## Goals
### Coding Conventions/Formatting
Generally, our main goal is to follow the “Power of 10: Rules for Developing Safety-Critical Code” developed by NASA. This can give you a general understanding of what will be expected when uploading code to our shared github.
### Function Format
A basic detailing of what functions are, what different aspects of functions do, and how they should be written. 

Functions are super simple. If you ever have code that is constantly needing to be copy pasted, it's better off being stored in a function, because that's essentially what they're meant for. Instead of putting the same code in different places, you call the function that contains the reusable code while the main code is running, causing the compiler to jump from the main code into your function.  
Function Declaration
Not super necessary but we’re gonna do it anyway for the sake of organization. This is telling the compiler what the function is, what its return type is, and what necessary data is needed to make the function work.

``` C
void myFunction(); 
// This tells the compiler that you have a function that:
// Void -> has no return type
// () -> has no necessary variables  
```
``` C
int myOtherFunction(int age, int name);
// This tells the compiler that you have a function that:
// Int -> returns an integer, a simple number with no decimals
// (int age, int name) -> has two variables, an integer named age and another integer names age
```

### Function Definition and Formatting
After declaring the function above, you can now make the definition alongside the function “body”.

### General Code Format
A basic detailing of what will be in each section of our code, what they do, and how they should be written.
``` C
// Start here, add names and all necessary copyright info
// The first few lines will be meant for all the constants in our system. This includes:

#include statements -> Libraries we need to make our code work
Ex: #include <stdio> // include the stdio library for standard input and output
                                 // all names are predefined because they’re the names of libraries

#define statements -> Values we will be using throughout the entire system
Ex: #define LED_1 11 // LED1 is assigned to pin 11 from now on
                                   // Naming convention: Always capital, underscores for spaces

Structures -> a way to group several related variables together
Ex: struct carletonStudent { // definition of the structure itself
           int studentNum; // all the necessary things that needs to be held within structure
           int studentName;
           float studentGpa;
      };
Function Declarations -> Basically define the function before we make it later
Ex: void myFunction(); // Precursor to making the definitions later
// We want to ensure the compiler knows about the function’s existence, including its name, return type, and expected arguments 
Enums -> A special type that's meant to represent a group of constants. This is basically where our states are gonna be put
Ex: enum { // type at the top
           IDLE = 0, // all states represented by a number, each state all caps
           CONNECTED = 1,
           BLOW_UP = 2
       } rocket_state_t; // name of the enum at the bottom

Other Constant type values -> This includes:
Volatile
Static
Const
etc.

// Once we have completed the declaration section, we move onto actually creating our functions
```


## Current Timeline
## Progress/Meeting Minutes

## State Diagram

RocketStateMachine.drawio.png


## Contributors
Azan Huggins Goolamallee, 101260082

