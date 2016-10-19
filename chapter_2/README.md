# Techshop EEE-201: Basic programming

## Chapter 2

In this chapter, we are going to start building circuits and using our Arduino to control those circuits; we will be covering the following topics in this chapter:

- blinking an LED with `digitalWrite()`
- variable type `byte`
- using a normally open (NO) switch 
- using a potentiometer to adjust the brightness of the LED

## Table of Contents

* [Introduction](#introduction)
    * [Current limiting resistors](#current-limiting-resistors)
* [Part 1](#part-1)
* [Part 2](#part-2)
* [Part 3](#part-3)


## Introduction

This chapter assumes you are some knowledge of how to read circuit diagrams; if you have never seen one before, head over to the [circuit diagram tutorial](https://github.com/ConstantinoSchillebeeckx/Techshop-EEE-201/tree/master/circuit_diagrams) to read all about 'em.

#### Current limiting resistors

Limiting current into an LED is very important. An LED behaves very differently to a resistor in circuit. Resistors behave linearly according to [Ohm's law](https://en.wikipedia.org/wiki/Ohm%27s_law): V = IR. For example, increase the voltage across a resistor, the current will increase proportionally, as long as the resistor's value stays the same. Simple enough. LEDs do not behave in this way. They behave as a diode with a characteristic [I-V](https://en.wikipedia.org/wiki/File:Diode-IV-Curve.svg) curve that is different than a resistor.

For example, there is a specification for diodes called the characteristic (or recommended) forward voltage (usually between 1.5-4V for LEDs). You must reach the characteristic forward voltage to turn 'on' the diode or LED, but as you exceed the characteristic forward voltage, the LED's resistance quickly drops off. Therefore, the LED will begin to draw a bunch of current and in some cases, burn out. A resistor is used in series with the LED to keep the current at a specific level called the characteristic (or recommended) forward current.

![circuit1](https://cdn.rawgit.com/ConstantinoSchillebeeckx/Techshop-EEE-201/master/chapter_2/image1.jpg)

Using the circuit above, you will need to know three values in order to determine the current limiting resistor value.

`i` = LED forward current in Amps (found in the LED datasheet)
`Vf` = LED forward voltage drop in Volts (found in the LED datasheet)
`Vs` = supply voltage

Once you have obtained these three values, plug them into this equation to determine the current limiting resistor:

![equation](http://latex.codecogs.com/gif.latex?R%3D%5Cfrac%7BV_%7Bs%7D-V_%7Bf%7D%7D%7Bi%7D)  

Also, keep in mind these two concepts when referring to the circuit above.
1. The current, `i`, coming out of the power source, through the resistor and LED, and back to ground is the same. [KCL](http://en.wikipedia.org/wiki/Kirchhoff%27s_circuit_laws#Kirchhoff.27s_current_law_.28KCL.29)
2. The voltage drop across the resistor, in addition to the forward voltage drop of the LED equals the supply voltage. [KVL](http://en.wikipedia.org/wiki/Kirchhoff%27s_circuit_laws#Kirchhoff.27s_voltage_law_.28KVL.29)

You can find a handy [resistor calculator](http://led.linear1.org/1led.wiz) online which will tell you exactly which resistor you should be using for your ciruit!


## Part 1 

basic blink sketch with digital pin

![circuit1](https://cdn.rawgit.com/ConstantinoSchillebeeckx/Techshop-EEE-201/master/chapter_2/Chapter-2-Part-1.svg)

## Part 2

adding in the switch
![circuit1](https://cdn.rawgit.com/ConstantinoSchillebeeckx/Techshop-EEE-201/master/chapter_2/Chapter-2-Part-2.svg)

## Part 3

using a potentiometer
![circuit1](https://cdn.rawgit.com/ConstantinoSchillebeeckx/Techshop-EEE-201/master/chapter_2/Chapter-2-Part-3.svg)
