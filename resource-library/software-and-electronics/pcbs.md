# PCBs

## Introduction

Printed Circuit Boards (PCB)s are a great way to make compact, robust, and far more efficient electronics. Instead of using wires, the circuity is etched into a sheet of copper supported on a fiberglass board.

## How PCBs Work

{% embed url="https://youtu.be/H9pGbLJknDk" %}
(Source: Techquickie @ YouTube.com)
{% endembed %}

## How PCBs Are Made

{% embed url="https://youtu.be/ljOoGyCso8s" %}
(Source: Strange Parts @ YouTubecom)
{% endembed %}

## Basics of Designing a PCB

{% embed url="https://youtu.be/35YuILUlfGs" %}
(Source: GreatScott! @ YouTube.com)
{% endembed %}

## EDA

Electronic Design Automation is where all Printed Circuit Board (PCB) projects start. It's basically like CAD but for circuit boards. The basic process is the same, you start by designing a schematic, then you convert it into a PCB outline, place the components, and trace the various connections.&#x20;

### Easy EDA

Easy EDA is a free and open-sourced web browser-based EDA software under the JLCPCB and LCSC's ecosystem. This makes designing and ordering the parts with their services extremely streamlined and easy. However, this also means if one would like to purchase components from other suppliers such as Digikey, a lot of the automatic features and libraries may not be accessible.&#x20;

{% embed url="https://easyeda.com/" %}

## Design References

The complexity of PCB projects has vastly decreased due to the amount of open source design references. If you are able to make a microcontroller and sensor project using breakout boards on a breadboard, you can easily design a PCB for it. One of the simple shortcuts is simply designing an adapter board PCB that takes in various breakout and avoids the mess of wires. However, a step above that would be to reference off of the various breakouts and replicate the schematic onto a PCB to make a fully integrated single board. An example of this procedure is, if one had an Arduino with an Adafruit pressure sensor breakout, they can wire the 2 components together and have a pressure reading circuit. If one wants to make this even more compact, they can then copy both the Arduino and adafruit sensor schematics into their EDA, then populate component by component into a single compact PCB layout of their choice. This is even easier thanks to big electronics companies providing all their references for free for you to adapt on, here are some examples we like using.

{% embed url="https://www.sparkfun.com/" %}
Click the breakout of interest, then go to documents, then schematics.
{% endembed %}

{% embed url="https://github.com/adafruit" %}
All of Adafruit's EDA files are up on their GitHub.
{% endembed %}
