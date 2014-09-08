---
layout: post
title: Electrical Properties
date: 2014-09-05 23:41:57
categories: jekyll update
---
Components have design specifications that results in a maximum tolerance for particular properties of electricity (i.e voltage or amperage). Fortunately, voltage (v), resistance (r), and amps (i) are all related by Ohm's law giving a formula of  v =ir . Another important property to consider is wattage (p), which is found with the formula p=i v=i^2 r. When attempting to determine whether or not a component is suitable for a particular circuit, it's necessary to verify the component's ratings, and adjust the circuit design accordingly.

There are two types of circuits: series circuits and parallel circuits. A series circuit is one where there is only one path that the power flows through. Parallel circuits have multiple paths for electricity to flow. 

Why does it matter that there is a difference in the number of pathways a circuit has? It's because it affects the resulting resistance. In a series circuit, the total resistance is equal to the sum of all of the resistors. Meanwhile in a parallel circuit, the total resistance requires a bit more work to calculate. Assuming there is only one resistor in each of the branches where the circuit splits into multiple pathways, total resistance is calculated by dividing 1 by the summation of resistance from each pathway. The resistance from a single pathway is determined by dividing 1 by the resistor value. So if we had 3 different pathways, total resistance would be 1/[(1/R1)+(1/R2)+(1/R3)].

"Then WTF happens if we combine series and parallel circuits???" In this case, we'd have a series-parallel circuit, in which case I'd ask you why do you hate yourself if you were using this to build a very basic circuit. In order to do this, you'd first calculate the total resistance from the parallel portion. After you attain that value, treat it like a series circuit and add it to the other resistance values.

"Bu-bu-but there are two resistors in one of the pathways of the parallel portion of the series-parallel." If there are 3 resistors where the first and second are in the same pathway, add the first and second, then treat it as a parallel so it looks like the following: total_resistance = 1/[(1/(R1+R2))+(1/R3)].

Why does total resistance matter? It's needed in order to determine other values such as current and voltage. It all leads back to tolerance and "will this component work there."
