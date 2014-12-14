---
layout: post
title: Into Arduino
date: 2014-09-08 00:35:26
categories: jekyll update
---
When working with Arduino, it's important to understand some of the outputs/inputs on the Arduino board as well as some of the core specification of its capabilities. To start, since we're using an <a href="http://arduino.cc/en/Main/arduinoBoardUno">Arduino Uno R3</a>, it has the following pins:

	1xIOREF
	1xReset
	1x3.3 V
	1x5 V
	2xGround
	1xVin
	6xAnalog Inputs
	14xDigital I/O (6 are PWM)

The ATMEGA328 microcontroller that drives the Arduino Uno R3 has a clock speed of 16MHz, 32KB of flash storage, 2KB of SRAM, and 1KB of EEPROM. "Are those powerful specs?" It can't run <a href="http://www.crysis.com/crysis-3">Crysis</a>, but it can drive fairly simple <a href="http://www.instructables.com/id/Build-an-autonomous-Wall-E-Robot/">robot</a>.

There are other Arduino variants such as the <a href="http://arduino.cc/en/Main/ArduinoBoardMega2560">Mega</a>, the <a href="http://arduino.cc/en/Main/ArduinoBoardLilyPad">LilyPad</a>, and the <a href="http://arduino.cc/en/Main/ArduinoBoardProMini">Pro Mini</a>. In addition to the other variants, there are also plugin <a href="http://arduino.cc/en/Main/ArduinoShields">"shields"</a> that extend the functionality of the Arduino to allow expansion from simple electronics all the way to web interfacing.
