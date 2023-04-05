---
description: A tutorial on learning how Arduino code works.
---

# Getting Started with Programming on an Arduino

## Introduction

As previously said with C++, it has a quite large learning curve that requires a lot of previous knowledge about how a computer works, how C works, how C++ works, etc., etc. But given one step at a time, it is significantly easier to learn with the Arduino framework than to go into the wild west of C++ programming.

If you're a total beginner stuck with an Arduino with no way to program it, no fear! This tutorial is for you. We here at Canine Rocket Technologies have had our own first experiences with Arduino. It isn't pretty, but it got us where we are now. Stick with us, we don't bite (too hard)!

## Part 1: Understanding How Code Works

In a nutshell, all a computer does is follow a list of basic instructions. These instructions can be called machine code, the ones and zeros defining what the computer should do. A higher level implementation of machine code is an assembely language, or a human representation of those ones and zeros.
Let's not jump too deep into that today, but try to keep that in mind as we go along this tutorial.

We will first be learning the basics of C, the precursor to the sister language C++. Both are very similar, but have very different features.

C is a high(ish) level programming language for general-purpose demands. It was created in the 1960s when the developers of the brand-new UNIX operating system got tired of writing assembly code and wanted something easier and more understandable to write in.

The basics of C and C-based programming languages follow these five main principles:
- Functions: A way to call different parts of code in a single line.
- Variables: A place to store all kinds of data in memory.
- Conditions: A way to branch code depending on different variables.
- Loops: A way to recursively run code without much effort.
- Operations: A way to perform mathmatical calculations with ease.

Let's examine each principle in context with some C code.

```c
#include <stdio.h> // Unrelated to what we're doing but required by C to do stuff.

int main()
{
	float x = 3.14;
	if (x > 4)
	{
		printf("x is greater than 4.\n");
	}
	else
	{
		printf("x is less than 4.\n");
	}
	for (int i = 0; i < 5; i++)
	{
		x += 2.16;
		printf("x is now %f.\n", x);
	}
	return 0;
}
```

Did you see each principle in action?

If not, here's a commented version of the same code.

```c
#include <stdio.h> // Unrelated to what we're doing but required by C to do stuff.

// Setting up the main function, it is ran on the start of the program.
int main()
{
	// Setting a floating-point variable x to 3.14.
	float x = 3.14;
	
	// Checking if x is greater than 4.
	if (x > 4)
	{
		// If it is, we call a function to say it is.
		printf("x is greater than 4.\n");
	}
	// If the condition above failed, code is executed here.
	else
	{
		// If x is not greater than 4, we call a function to say it is less than 4.
		printf("x is less than 4.\n");
	}
	
	// Looping 5 times to increment the value of x by 2.16 and print the new value
	// out each time.
	
	// It works by creating a temporary variable called i to hold which iteration
	// we are in. Each time we start the loop, we compare the value of i to a
	// number, 5 in this case. If we have exceeded this number, we stop the loop
	// and continue after this loop. If we have not, we increment i and run the
	// code in the loop.
	for (int i = 0; i < 5; i++)
	{
		// Do the increment.
		x += 2.16;
		// Print the new value by passing x as a parameter to the function.
		printf("x is now %f.\n", x);
	}
	
	// Finish the function by returning 0, the operation code that the program
	// finished successfully.
	return 0;
}
```

Of course, there's still a lot more to C than just this. This is a basic understanding of how C works.

This is essentially what we are doing in the code:
- We set up the `main` function. It is the function to run at the start of the program.
- We create a floating-point variable `x`. That means it can accurately store a number that has a tenths place, hundredths place, etc.
- We check to see if `x` is greater than four. If it is, we print to the console it is. If not, we print to the console it isn't.
- We create a loop to increment the value of `x` by `2.16` five times. We then print the current value of `x`.
- We finish off by returning `0` from the `main` function. This tells the operating system that the program finished successfully.

By compiling this code with your favorite compiler and running it, the output should look similar to this:
```
x is less than 4.
x is now 5.300000.
x is now 7.460000.
x is now 9.620000.
x is now 11.780000.
x is now 13.940000.
```

Congratulations, you have learned the basic principles of how (most) programming languages work. Good job.

## Part 2: Implementing Our Own Arduino Code

Now that we've seen how basic C code is, let's try making our own C++ code to do some Arduino things.
For now, we will keep it basic so we can easily understand how it works.

Just like with the C code, here is some C++ code to do some Arduino things:
```c++
#include <Arduino.h> // Like the first line in the C code. It is required by Arduino
                     // to do stuff.

const int pin = 13;

void setup()
{
	Serial.begin(9600);
	Serial.println("Hello, world!");
	
	pinMode(pin, OUTPUT);
}

void loop()
{
	digitalWrite(pin, HIGH);
	delay(500);
	digitalWrite(pin, LOW);
	delay(500);
}
```

Many, but not all, of the principles states in Part 1 were used. Can you spot them?

If not, here's a commented version of the same code.

```c++
#include <Arduino.h> // Like the first line in the C code. It is required by Arduino
                     // to do stuff.

// Create a constant variable pin and set it to the value 13.
// A constant variable is like a regular variable but it cannot change.
const int pin = 13;

// Define the setup function. This function runs once at the start of the Arduino
// being turned on.
void setup()
{
	// Set up the serial line between the Arduino and computer at 9600 baud.
	Serial.begin(9600);
	// Send a string through the serial to say hello.
	Serial.println("Hello, world!");
	
	// Set the pin mode of our pin (definied above) to an output state.
	// This means that we can set the value of the pin to HIGH or LOW.
	// Likewise, we can reverse this and get an input state. It does what
	// you expect, we can read the value of a pin.
	pinMode(pin, OUTPUT);
}

// Define the loop function. This function runs after the setup funciton, but it will
// always be called, even if it's finished.
void loop()
{
	// Write the value of our pin to HIGH. Basically turn it on.
	digitalWrite(pin, HIGH);
	// Wait 500 milliseconds, or half a second.
	delay(500);
	// Write the value of our pin to LOW. Basically turn it off.
	digitalWrite(pin, LOW);
	// Wait another 500 milliseconds.
	delay(500);
}
```

If you couldn't tell already, this code turns on and off an LED on the Arduino really quickly.

If you would like a list of more functions to play with, [here's](https://www.arduino.cc/reference/en) a complete list that Arduino gives us to play with.
