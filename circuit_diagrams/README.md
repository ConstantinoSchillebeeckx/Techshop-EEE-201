# Techshop EEE-201: Basic programming

## Circuit diagrams

Adapted from [Sparkfun](https://learn.sparkfun.com/tutorials/how-to-read-a-schematic/schematic-symbols-part-1)


## Introduction

Schematics are our map to designing, building, and troubleshooting circuits. Understanding how to read and follow schematics is an important skill for any electronics engineer.

This tutorial should turn you into a fully literate schematic reader! We’ll go over all of the fundamental schematic symbols:

![img](https://cdn.sparkfun.com/assets/6/8/6/d/1/51cdc767ce395f7558000002.png)

Then we’ll talk about how those symbols are connected on schematics to create a model of a circuit. We’ll also go over a few tips and tricks to watch out for.


## Schematic Symbols (Part 1)
Are you ready for a barrage of circuit components? Here are some of the standardized, basic schematic symbols for various components.

### Resistors

The most fundamental of circuit components and symbols! Resistors on a schematic are usually represented by a few zig-zag lines, with two terminals extending outward. Schematics using international symbols may instead use a featureless rectangle, instead of the squiggles.

![img](https://cdn.sparkfun.com/assets/2/2/6/9/c/51cc9e55ce395f576d000000.png)

#### Potentiometers and Variable Resistors

Variable resistors and potentiometers each augment the standard resistor symbol with an arrow. The variable resistor remains a two-terminal device, so the arrow is just laid diagonally across the middle. A potentiometer is a three-terminal device, so the arrow becomes the third terminal (the wiper).

![img](https://cdn.sparkfun.com/assets/4/5/c/a/0/51cc9e55ce395fad69000001.png)

### Capacitors

There are two commonly used capacitor symbols. One symbol represents a polarized (usually electrolytic or tantalum) capacitor, and the other is for non-polarized caps. In each case there are two terminals, running perpendicularly into plates.

![img](https://cdn.sparkfun.com/assets/9/c/9/c/5/51cc9e55ce395fcd6c000000.png)

The symbol with one curved plate indicates that the capacitor is polarized. The curved plate represents the cathode of the capacitor, which should be at a lower voltage than the positive, anode pin. A plus sign might also be added to the positive pin of the polarized capacitor symbol.

### Inductors

Inductors are usually represented by either a series of curved bumps, or loopy coils. International symbols may just define an inductor as a filled-in rectangle.

![img](https://cdn.sparkfun.com/assets/3/f/a/4/0/51cca0f8ce395fa06c000001.png)

### Switches

Switches exist in many different forms. The most basic switch, a single-pole/single-throw (SPST), is two terminals with a half-connected line representing the actuator (the part that connects the terminals together).

![img](https://cdn.sparkfun.com/assets/3/5/4/2/a/51cc9e55ce395fa969000002.png)

Switches with more than one throw, like the SPDT and SP3T below, add more landing spots for the the actuator.

![img](https://cdn.sparkfun.com/assets/f/a/b/3/3/51cc9e55ce395f7a6c000001.png)

Switches with multiple poles, usually have multiple, alike switches with a dotted line intersecting the middle actuator.

![img](https://cdn.sparkfun.com/assets/0/a/4/0/7/51cc9e55ce395fb072000000.png)

### Power Sources

Just as there are many options out there for powering your project, there are a wide variety of power source circuit symbols to help specify the power source.

#### DC or AC Voltage Sources

Most of the time when working with electronics, you’ll be using constant voltage sources. We can use either of these two symbols to define whether the source is supplying direct current (DC) or alternating current (AC):

![img](https://cdn.sparkfun.com/assets/4/7/b/0/3/51cc9e55ce395f8f6d000001.png)

#### Batteries

Batteries, whether they’re those cylindrical, alkaline AA’s or rechargeable lithium-polymers, usually look like a pair of disproportionate, parallel lines:

![img](https://cdn.sparkfun.com/assets/b/a/5/0/8/51cc9e54ce395ff06d000001.png)

More pairs of lines usually indicates more series cells in the battery. Also, the longer line is usually used to represent the positive terminal, while the shorter line connects to the negative terminal.

#### Voltage Nodes

Sometimes – on really busy schematics especially – you can assign special symbols to node voltages. You can connect devices to these one-terminal symbols, and it’ll be tied directly to 5V, 3.3V, VCC, or GND (ground). Positive voltage nodes are usually indicated by an arrow pointing up, while ground nodes usually involve one to three flat lines (or sometimes a down-pointing arrow or triangle).

<p align="center">
![img](https://cdn.sparkfun.com/assets/f/7/5/4/2/51cc9e55ce395fcc74000000.png)
</p>
