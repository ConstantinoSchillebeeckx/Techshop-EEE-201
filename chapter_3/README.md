# Techshop EEE-201: Basic programming

## Chapter 3

This is the last chapter of this course, so let's make it interesting!  We're going to be learning about all sorts of things including:
- Analog input
- Fading a LED with PWM
- variable type `int`
- `if` control structure

## Table of contents

TODO

## Introduction

TODO

## Part 1 - analog inputs

In [Chapter 2](https://github.com/ConstantinoSchillebeeckx/Techshop-EEE-201/tree/master/chapter_2) we used the **output** of a digital pin to control the blinking of a LED; in this first part we are going to be looking at inputs.  But not just any type of input, we're going to be using an analog input.  Previously, we see that we could set the digital pin to either `HIGH` or `LOW`; that is, it could be set to only two values.  An analog pin is different in that it can have many values, in our case, 1024 to be exact!  Let's begin with an example; the circuit we want is shown below, and the sketch your after is [AnalogInput.ino](https://github.com/ConstantinoSchillebeeckx/Techshop-EEE-201/blob/master/chapter_3/AnalogInput.ino).

<p align="center">
    <img src="https://cdn.rawgit.com/ConstantinoSchillebeeckx/Techshop-EEE-201/master/chapter_3/Chapter_3-Part_1_bb.svg">
</p>

Let's break the sketch down by looking at the top part first.
```c
byte sensorPin = A0;    // select the input pin for the potentiometer
byte ledPin = 13;      // select the pin for the LED
int sensorValue = 0;  // variable to store the value coming from the sensor

void setup() {
  // declare the ledPin as an OUTPUT:
  pinMode(ledPin, OUTPUT);
  // because the analog pins are always INPUT, we don't have to declare it as such
}
```

In the first three lines, we declare three variables, two `byte` types and one [`int`](https://www.arduino.cc/en/Reference/Int) type.  Previously, we saw that a `byte` is a number that can be any value between 0 and 255 (inclusive); `int` (which stands for integer) is another type of number, but it's much bigger; it's a 16-bit number which equates to 2^16.  Bust out the calculator and you'll see that equals 65,536!  However, an `int` is special in that it can hold negative values, in fact an `int` can hold the values -32,768 to 32,767; for those that are observant you can see that 32,767 + 32,768 = 65,535 (can anyone tell me what that isn't exactly equal to 2^16?).  The reason we want to declare the variable `sensorValue` as an `int` is because the range we expect it to be reading from is 0 to 1023 (the range of the analog pins).

In the `setup()` function we see that we are setting the `ledPin` (pin 13) as an `OUTPUT`.  Note that we don't have to define the analog pin as an input because it can only act asn an input.  Let's move on to the interesting parts:

```c
void loop() {
  // read the value from the sensor:
  sensorValue = analogRead(sensorPin);

  // turn the ledPin on
  digitalWrite(ledPin, HIGH);

  // stop the program for <sensorValue> milliseconds:
  delay(sensorValue);

  // turn the ledPin off:
  digitalWrite(ledPin, LOW);

  // stop the program for for <sensorValue> milliseconds:
  delay(sensorValue);
}
```

In the `loop()`, we see a function we haven't seen before [`analogRead()`](https://www.arduino.cc/en/Reference/AnalogRead) - this is the function which will be reading the input values on our analog pin (pin A0).  As we mentioned previously, we expect this value to be anywhere between 0 and 1023 (inclusive).  The remaining lines of code we've seen in Chapter 2: we turn our LED on with `digitalWrite()`, then we pause the sketch by a value of `sensorValue` number of milliseconds, then we turn off our LED with `digitalWrite()` and then we pause again.  The interesting part here is that, instead of pausing with a fixed amount, we can control the length of pause with the value that is read by `analogRead()` which we control with the trimpot.  That means, we can directly control how fast our LED blinks just by twisting the trimpot to different values!

**Explore:** how would we change our sketch to see what value our variable `sensorValue` is set to?


## Part 2 - PWM digital output

PWM

## Part 3 - Putting it all together

if statment reading the analog input to turn on RGB channel on, off
switch to control another RGB channel
blink on another channel

