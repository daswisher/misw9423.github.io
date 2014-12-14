---
layout: post
title: Breaking Down the <strike>House!</strike> Laptop
date: 2014-08-29 19:59:38
categories: jekyll update
---
Today, I was tasked with breaking apart something electronic in my house. Luckily, I already have the wall in my office area decorated with a dismantled laptop :D
Needless to say, let's get into it!
While there are a bunch of parts to look at, I unfortunately had to throw away some components since there was no way to hang a heavy @#$ battery on the wall. To begin, we can see in this first image that we have the motherboard, a usb controller card, a keyboard, hard drive controller cards (HDD platter+head), the webcam, speakers, wireless modules, and the microphone. {Yes, that's a portion of the LCD panel at the top of the image}.
![](/assets/ComputerP1.jpg)

Looking a little closer at the motherboard, we can see our components a little better. Thanks to the many advancements in technology, it's not incredibly easy to see a specific individual part immediately and be able to replace it. Some of the major parts you'll find connected on this board are the processor and graphic processor (CPU and GPU) located under the copper heatsink, a couple sticks of memory (RAM), the black hard drive (HDD) serial ATA (SATA) port, an ethernet port (RJ45), audio connectors (3.5 mm audio jacks), and the external display connector (VGA).


![](/assets/ComputerP2.jpg)

<h2>BASIC COMPONENTS!!!</h2>

Here's a look at the external display connector.

![](/assets/vgaf.jpg)

This is the onboard battery. Most people ask, "Why the hell do I need a battery in muh compooter?" It's for the Real Time Clock (RTC) that keeps track of time while the computer is off...NEAT :D

![](/assets/batteryf.jpg)

The 3 silo looking things in the picture below are capacitors. 

![](/assets/capacitorsf.jpg)

This is an integrated circuit (IC).

![](/assets/icf.jpg)

There are a bunch of parts in this picture, but the ones that are easiest to spot out are the resistors. Those are going to be the copperish looking pills. Glancing over at the other components, it looks like there are also some ICs, transistors, a relay, and maybe some small capacitors. The little circles (towards the lower right quadrant) are holes that can be used with through-hole-technology (THT) components even though most of the parts you'll find are surface-mount-devices (SMD).There are reasons why you'd use SMD over THT and vice versa.

![](/assets/resistorsf.jpg)

<table border="1">
	<tr>
		<th align="left">
			Reasons for THT:
		</th>

		<th align="left">
			Reasons for SMD:
		</th>
	</tr>

	<tr>
		<td>
			Easier to replace/install by hand
		</td>
		<td>
			Smaller than THT implementation
		</td>
	</tr>
	<tr>
			<td></td>
			<td>
				More efficient to add a large number of components since it uses a heating process with solder paste
			</td>
	</tr>
	<tr>
		<td></td>
			<td>
				Not as destructive since it doesn't reduce the mounting surface area like THT, small size helps for maximizing components per printed circuit board (PCB), and they normally utilize both of the sides of the PCB instead of just one.
			</td>
		
	</tr>
</table>
