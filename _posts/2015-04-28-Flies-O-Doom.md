---
layout: post
title: Flies-O-Doom
date: 2015-04-28 02:27:34
categories: jekyll update
---
Project goals: 
1 Project: A flying remote control quadcopter
Understand components for flight controls
Learn mechanics: load balancing, torque, orientation, flight
Understand troubleshooting with quadcopter
Documentation once at hover

Stretch goal:
Implement own flight controls
UAV

Misc:
Figure out battery issue
Puppy drone
lost?

-------------------------------------------------------------------------------
Introduction:
With the proliferation of unmanned aerial vehicles (UAVs), especially with the US military, there has been a growth in public communites with the usage of aerial vehicles manned and unmanned. Helicopters and once ruled hobbyist skies, but tide has turned in favor of quadcopters. 

Components:
Frame
	This is the core to everything. The frame holds all of the components. Things to consider when choosing a frame are the size, weight, and materials because they can affect how the 'copter will fly and most certainly how it'll handle impacts during collisions and crashes.
Motor x 4
	In tandem with the propellers, motors are what drive lift. A motor's power rating will also dictate the minimum specification when selecting an ESC. Most sites will give feedback on recommended ESC and propeller specs to pair with the motor.
Electronic Speed Controller (ESC) x 4
	The ESC will dictate how fast the motors spin. A common firmware that's used is the SimonK. Firmware is important because it can affect the refresh rate of ESC and how precisely the ESC can control the motors.
Flight Controller Board
	Flight controllers are the brains of the system. Interfacing the sensors, motor control speed control, as well as inputs, flight controllers are where the magic happens.
Radio Transmitter and Reciever (Tx/Rx)
	Without the Tx/Rx, the quadcopter can't be remotely controlled. It's safe to say that they're kind of important.
Propeller x 4 (clockwise [cw] x 2 and counter-clockwise [ccw] x 2)
	Fans move air; air makes thrust; thrust moves thingies.
Battery
	Power anybody?
Charger
	Refill anybody?

Flight Mechanics:
Before you begin flying, there's a bit of studying to do before going full throttle. Needless-to-say, it wouldn't hurt to refresh on some basic physics to learn about flight dynamics. One important concept to understand is torque/momentum in addition to the laws of conservation. Imagine you are sitting on a chair, without your feet touching the ground. You're also holding a bicycle wheel (axle perpendicular to the floor) spinning ccw. If you were to stop the wheel, you'd begin to start spinning ccw due to the conservation of momentum. In order to determine how the quadcopter will spin in air (yaw), we have to take the sum of momentums (ccw + cw) from our motors. This is why in the component list, there are 2 cw + 2 ccw propellers because we need counter-rotating rotors in order to have a net spin of 0. So if we wanted to rotate our quadcopter ccw, this means that the quadcopter must slow the ccw spinning rotors to maintain conservation of momentum. The next question becomes, "What happens if I lower the speed of one side of the quadcopter?" The answer is simple; it'll tilt towards the direction with the lower speed which will cause it to fly in that same direction. The final question is "If I have both of my ccw rotors on one side and cw rotors on the other, what will happen?" If you were to change yaw, not only would you spin, but you'd decrease thrust on one side causing the whole quadcopter to spin out of control. In an ideal configuration, there should be an alternating pattern of cw+ccw going around the propellers.

Abstract:
The purpose of this project is to serve as a preface to swarm technology in addition to dynamic networking and SLAM (simultaneous localization and mapping) technologies. By working with Crazyflie, it provides the opportunity on how flight mechnaics work on a small scale, and allows for flexible development with the variety of components and its options of supported programming languages.

About Crazyflie 2.0:
The Crazyflie 2.0 is a micro quadcopter (weighing in at 27g) with a size of 92mmx92mmx29mm. It can communicate on 2.4 gHz and Bluetooth Low Energy (BTLE). Sensors it includes are 3 axis gyro, accelerometer, and magnetometer. It has a 7 minute flight time [using the 240mAH LiPo battery] and has a max recommended payload of 15g. Since the Crazyflie using coreless motors, it doesn't need ESCs.

Setup:
Putting the quadcopter was fairly straight forward. All I had to do was place the motors into the motor mounts, slide the mounts onto the PCB, then plug the motors into the sockets on the arm. After, I attached the battery and mounted it on top using the the pin/perfboard securement that's used. Since the Crazyradio PA and debugging kit weren't available when the Crazyflie arrived, I had to resort to using my old Samsung Galaxy S4 that I keep around for tinkering and development. By using my old phone, I was able to control the quadcopter via bluetooth and fly it via that method. Once the USB dongle arrived, I was able to begin receiving data from the Crazyflie's onboard sensor to my computer wirelessly. 

Issues:
DO NOT PAIR WITH CRAZYFLIE VIA BLUETOOTH! When I tried flying on my own without my friend, I couldn't connect to the Crazyflie via bluetooth. I tried an array of devices including my Samsung, to iPhones (4-6+), and found that the only devices that worked were the Nexus 5 and HTC M8. Reason being is that using the mobile clients, if you pair with the Crazyflie with the phone, it causes an issue with the app where it can't connect to the quadcopter oddly. 

UPDATE IMMEDIATELY! While trying to learn how to fly late one night (failing miserably might I add), the quadcopter would shut off mid flight and dive straight into the pavement. I thought I simply did not know how to keep track of time and that the battery was dead. Apparently in the stock firmware for the Crazyflie 2.0, there is an issue with quick changes in thrust that causes the voltage regulators to become overloaded. The result is that the system gets overloaded and shuts off entirely. Updating the firmware to the lastest version fixed the issue, and also improved flight stability which is awesome for noobie pilots =^-^=

INSTALL ALL THE DRIVERS! To get the desktop client to work, it's necessary to download and install the Crazyradio drivers. 
HAVE ALL THE FUNS!!! Nuff said. Let the doom ensue #Skynet


After finally learning how to control the quadcopter, I decided to try to benchmark battery life and performance. The process was fairly simple where I would charge the battery fully, crank the thrust to max to 

