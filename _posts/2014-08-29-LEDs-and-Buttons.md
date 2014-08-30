---
layout: post
title: LEDs & Buttons
date: 2014-08-29 20:12:39
categories: jekyll update
---
Thanks to the <a href="http://arduino.cc/en">Arduino</a> website, there are a series of projects that users can build from the tutorials that are posted. Today, we're starting with the basics of I/O using LEDs and buttons. 

Note: I'm a bit lazy and decided to bypass adding cables to the pos/neg rails on the breadboard and hooked components directly into the power outputs. I also adjusted my code to work with pin 9 instead of pin 13 because why not...nuff said

The first tutorial that we have is the <a href="http://arduino.cc/en/Tutorial/BareMinimum">Bare Minimum</a> tutorial. This is pretty simple because it's the easiest and the most energy efficient...as in you don't need to plug it in. It simply describes the process for creating programs for Arduino. There are 2 major components which are the setup and loop functions. The code will appear as follows in all Arduino programs...

{% highlight ruby %}
void setup()

void loop()

{% endhighlight %}

![Arduino](/assets/BareMinimum.jpg)

<a href="http://arduino.cc/en/Tutorial/Blink">Blink</a> is the part where we actually begin hooking things up to the Arduino board. we have an LED on a 220 ohm resistor connected to pin 9 on the Arduino. The point of this tutorial is to demonstrate how output works and apply it to an LED. This project turns the LED on and off with a {% highlight ruby %}delay(1000){% endhighlight %} where the 1000 is the number of milliseconds the delay will last each time the LED is toggled.

![](/assets/Blink.jpg)

<a href="http://arduino.cc/en/Tutorial/DigitalReadSerial">Digital Read Serial</a> is where we begin to work with input. Buttons generally only output binary values: 0 for off/false, 1 (or any non-zero value) for on/true. After we open up the <a href="http://arduino.cc/en/guide/Environment">Serial Monitor</a>, we can view the state of the button to check whether or not it is being pressed. Since the delay is so small, it's possible to observe <a href="http://en.wikipedia.org/wiki/Switch#Contact_bounce">bouncing</a>. When using a button for input, there are two common ways to avoid interference from bouncing (this is called "debouncing").

Method 1: Setup a <a href="http://en.wikipedia.org/wiki/Pull-up_resistor">pull-down</a> circuit and add a capacitor.

Method 2: Add a delay() after the state of the button input changes.
The second method mentioned is the more common implementation because it doesn't require any extra components and is fairly simple to do.

![](/assets/DigitalReadSerial.jpg)

Just like blink, <a href="http://arduino.cc/en/Tutorial/Fade">Fade</a> works by using an LED and turning it on and off. The difference though is that it does it via pulse width modulation (PWM). Simply this just means that it's toggling the state of the output so fast that the eye interprets the light from the LED as a specific brightness. This project demonstrates the use of PWM and creates a simple "breathing" effect using the LED.

As its name implies, <a href="http://arduino.cc/en/Tutorial/BlinkWithoutDelay">Blink Without Delay</a> is more of a demonstration of code and how to bypass using the delay function and still create delays within the program.

<a href="http://arduino.cc/en/Tutorial/Button">Button</a> is where we combine both of the worlds of input and output (I/O) to create a simple interaction a user and hardware. When the user presses the button, the light will turn on and stay on until the user releases the button. 

![](/assets/Button.jpg)
