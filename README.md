# Grzmot-Mine
Introduction:

Grzmot is a nonlethal explosive mine. It's used to gain more information about the enemy's location during a siege. Imagine a hostage needs rescuing, but the position within the house is unknown. As a sentinel, you would want to cover your back from an ambush. The Grzmot mine has your back! It detects the heat radiated from humans in the infrared spectrum of light within a specific range. A short concussive burst from an explosive will disorientate the enemy and reveal his location. This mine can be attached to any surface during entry.This project is inspired by a game called 'Tom Clancy's Rainbow Six Siege'

Block Diagram:

![Grzmot Mine BD](https://user-images.githubusercontent.com/61559101/133403329-3741a4fc-66f9-48f4-8670-c9748fe78384.gif)

 The above figure shows the basic block diagram of the Grzmot mine. 
 
🔺The Infrared Radiation(IR) from any human will be detected by the Passive Infrared(PIR) sensor.

🔺A pair of pyroelectric sensors beside each other pick up the radiation.

🔺When the signal differential between the two sensors changes (when a person comes in range), the sensor will activate.

🔺This high signal is fed to the input of the NE555 timer circuit, which determines how long the ignition source must be on.

Working:

The NE555 time is configured in monostable mode.

![Grzmot-Mine-Enlarged](https://user-images.githubusercontent.com/61559101/134760760-1178e263-dc88-4f69-9be4-3c72e65a9a80.gif)
