# Techshop EEE-201: Basic programming

## Chapter 1

Explain the Arduino IDE and what a sketch is.


- `setup()`
- `loop()`
- `println()`
- using comments
- variable type `string`


## Part 1

Let's get started!  Open the Arduino IDE and copy/paste the [BaseMinimum.ino](https://github.com/ConstantinoSchillebeeckx/Techshop-EEE-201/blob/master/chapter_1/BareMinimum.ino) sketch.  You should see two sections of code, the first looks like:
```c
void setup() {
  // put your setup code here, to run once:

}
```
The `setup()` function is called when a sketch starts. Use it to initialize variables, pin modes, start using libraries, etc. The setup function will only run once, after each powerup or reset of the board.

Next we see the `loop()` section of the sketch:
```c
void loop() {
  // put your main code here, to run repeatedly:

}
```
The `loop()` function does precisely what its name suggests, and loops consecutively, allowing your program to change and respond as it runs. Code in the `loop()` section of your sketch is used to actively control the board.

Any line that starts with two slashes (//) will not be read by the compiler, so you can write anything you want after it. The two slashes may be put after functional code to keep comments on the same line. Commenting your code like this can be particularly helpful in explaining, both to yourself and others, how your program functions step by step.

## Part 2

So far we haven't actually done anything with the Arduino, let's fix that!  We begin with the quintessential [*Hello, World!*](https://en.wikipedia.org/wiki/%22Hello,_World!%22_program) example; copy/paste [HelloWorld.ino](https://github.com/ConstantinoSchillebeeckx/Techshop-EEE-201/blob/master/chapter_1/BareMinimum.ino) into your IDE now.
