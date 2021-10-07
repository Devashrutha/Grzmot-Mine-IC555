# Grzmot-Mine
INTRODUCTION:

Grzmot is a nonlethal explosive mine. It's used to gain more information about the enemy's location during a siege. Imagine a hostage needs rescuing, but the position within the house is unknown. As a sentinel, you would want to cover your back from an ambush. The Grzmot mine has your back! It detects the heat radiated from humans in the infrared spectrum of light within a specific range. A short concussive burst from an explosive will disorientate the enemy and reveal his location. This mine can be attached to any surface during entry.This project is inspired by a game called 'Tom Clancy's Rainbow Six Siege'

BLOCK DIAGRAM:

 ![Grzmot Mine BD](https://user-images.githubusercontent.com/61559101/133403329-3741a4fc-66f9-48f4-8670-c9748fe78384.gif)

 The above figure shows the basic block diagram of the Grzmot mine. 
 
🔺The Infrared Radiation(IR) from any human will be detected by the Passive Infrared(PIR) sensor.

🔺A pair of pyroelectric sensors beside each other pick up the radiation.

🔺When the signal differential between the two sensors changes (when a person comes in range), the sensor will activate.

🔺This high signal is fed to the input(negative edge triggered) of the NE555 timer circuit, which determines how long the ignition source must be on.

WORKING:

 ![IC555](https://user-images.githubusercontent.com/61559101/134848590-44b1dce3-3aee-42d4-b397-8f90ec5028e4.PNG)
“Image from https://www.electronics-tutorials.ws/waveforms/555_timer.html .”

NE555 was developed by 'Signetic Corporation' which was also called as SE555. It's mainly used in oscillator, pulse generator, or timer circuits consisting of 8-pins as shown in the figure below. It has an operating voltage around 4.5V to 15V. It's main function is to generate an accurate pulse. The '555' comes from the three 5kΩ resistors which are responsible for dividing the voltage(1/3Vcc and 2/3Vcc). There are two comparators, a SR flipflop, a npn and a pnp transistor. The simulation below shows the timer in mono-stable mode. 

SIMULATION:
![Grzmot-Mine-Enlarged](https://user-images.githubusercontent.com/61559101/134760760-1178e263-dc88-4f69-9be4-3c72e65a9a80.gif)
🟩- Output across the capacitor, 🟦- Output pulse at pin no 3.

🔺In the monostable mode the output of the timer is either 0 or 1 that is it has only one stable state.

🔺The amount of time for which the output must be high is determined by the value of thr resistor and capacitor connected in         series between Vcc, pin no 7&6 and ground as shown in the simulation below.

🔺Time(sec)=1.1xRxC. For the circuit below T = 1.1x10Kx500uF = 5.5seconds.

🔺At the output of the timer a bjt is placed in common emitter mode which acts as a switch. This drives the relay of the step up     transformer. The secondary turns is exposed which creates a high voltage, high temperature arc. This arc is used to ignite the     explosive. 

Visit https://www.electronicsforu.com/technology-trends/learn-electronics/555-timer-working-specifications for more details on the other modes of working of the IC555.

MECHANICAL CONSTRUCTION:

![3D CAD pictures](https://user-images.githubusercontent.com/61559101/134858967-0b48f912-5688-4491-9ded-ecdf60b09c1a.PNG)

The above CAD models were designed in Autodesk Fusion 360 and later 3D printed. PLA(Polylactic Acid) was used to have a balance between structural integrity and cost.
The Cap(Figure 1) holds the explosive while the Inner Shell(Figure 7) holds all the electronics. The Outer Shell(Figure 6) and the Tail(Figure 5) provide more rigidity.
The picture below shows the final construction of the prototype with and LED strip to show the activation of the mine. The entier prototype is powered by thw 18650 LiPo batteries(red) and the step-up transformer is placed outside to avoid any interference with the electronics inside.

![image](https://user-images.githubusercontent.com/61559101/136333376-37234641-5c6c-4839-a0fd-80a18be6e4b6.png) 

https://user-images.githubusercontent.com/61559101/136339074-43dbc6a6-f7aa-4313-a9ad-af6e772322d3.mov


FUTURE SCOPE:

🔺The Chemistry required for the mine to sick to any surface upon activation needs to be developed.

🔺The Grzmot Mine can be a useful military tool, used as an alerting system for detection of enemies in restricted areas.

🔺It can also be used in farms for avoiding animals which cause harm to the yields i.e. by placing Grzmot Mine in farms, and whenever the motion of any animal/bird is detected it will produce a large sound which will disturb the animal and will go away.


