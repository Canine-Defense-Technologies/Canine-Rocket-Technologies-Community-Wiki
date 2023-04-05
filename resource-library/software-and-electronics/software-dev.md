---
cover: ../../.gitbook/assets/chris-ried-512801-unsplash.jpg
coverY: 0
---

# Software Development Tools 1

## Introduction

Software is how our projects come alive. Although our primary focus is not software, we still use a variety of open-source tools to manage the software onboard our projects. Below are software packages and tools that we have used to write, test, debug, and load software for our projects.&#x20;



## Integrated Development Environments (IDEs)

### Arduino IDE

Anything microcontroller-related can usually be done with the Arduino Integrated Development Environment (IDE). Although it is recommended for smaller projects, it comes with many software examples and tools to help beginners and professionals alike to write, test, debug, and load software onto microcontrollers. Tools such as the Serial Monitor and Serial Plotter are crucial for testing.&#x20;

{% embed url="https://www.arduino.cc/en/software" %}

### Arduino Web Editor

This is just like the Arduino IDE that can be downloaded and installed, except it is run in a web browser. Although limited, it is still very powerful and useful for many applications, such as on-the-go projects or for learning beginners. In fact, it has helped us with our own projects while we were away from the lab.

{% embed url="https://docs.arduino.cc/learn/starting-guide/the-arduino-web-editor" %}

### Visual Studio Code

Amid its flaws, Visual Studio Code is a (somewhat) free and open-source Integrated Development Environment (IDE). It can handle dozens of languages, syntaxes, configurations, and plugins. Languages such as Python and C++ can be analyzed and ran on the fly. Plugins such as PlatformIO can build, test, and debug microcontroller code all from the comfort of Visual Studio Code.

## Languages

### C++

C++ is the main choice for our software projects, mainly for its stability and robust nature. Although it has a steep learning curve, C++ is a very powerful language that encompasses other useful features. It is very commonly used for microcontrollers and is, in fact, the language in which the Arduino IDE uses.

{% embed url="https://www.programiz.com/cpp-programming" %}

### Python

Although not used to run on microcontrollers (most of the time), Python is a great tool to automate tasks and perform calculations. Many simulators and other free and open-source projects are written using Python. It especially pairs well with smaller (but not microcontroller level) computers, such as the Raspberry Pi.&#x20;

{% embed url="https://www.python.org/downloads" %}

## Other Software Tools

### PlatformIO

PlatformIO is kind of like the Arduino IDE, but it is more professionaly-driven and has more complicated but configurable aspects to it. It can be installed with Visual Studio Code (another Integraded Development Environment, described above) or it can be installed for the command-line. Either way, it's a great tool for professionals and large/complicated projects.

{% embed url="https://docs.platformio.org/en/stable/home/index.html" %}
