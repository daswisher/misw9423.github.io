---
layout: post
title: Electrical Properties
date: 2014-08-31 23:11:44
categories: jekyll update
---

When working with Arduino, it's important to understand some of the outputs/inputs on the Arduino board as well as fundamental properties of electricity. To start, since we're using an Arduino Uno R3, it has the following pins:

	1xIOREF
	1xReset
	1x3.3 V
	1x5 V
	2xGround
	1xVin
	6xAnalog Inputs
	14xDigital (6 are PWM)

In regards to electricity, components have design specifications that results in a maximum tolerance for particular properties of electricity (i.e voltage or amperage). Fortunately, voltage (v), resistance (r), and amps (i) are all related by Ohm's law giving a formula of v=i*r. Another important property to consider is wattage (p), which is found with the formula p=i*v. When attempting to determine whether or not a component is suitable for a particular circuit, it's necessary to verify the component's ratings, and adjust the circuit design accordingly.

Example: There is an LED that is rated for 3.3 v that is to be implemented within a series circuit, but our input voltage is 5 v. What component would be needed to make the implementation possible?

There are two types of circuits: series circuits and parallel circuits. A series circuit is one where there is only one path that the power flows through. Parallel circuits have multiple paths for electricity to flow. One thing to remember when there are multiple pathways for electric to flow is that it will go through the path that provides the least resistance.
