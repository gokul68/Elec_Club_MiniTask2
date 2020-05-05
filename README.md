# Elec_Club_MiniTask2
# 1. Smart Glove Computer Mouse
## Problem Statement:-
A smart glove that functions as a mouse which you can control by moving your hand in the air.

## Ideation:- 
Currently, the project makes use of a Binho Qwiic Interface board and a Qwiic accelerometer. However, I think that this is unnecessarily complicated and that this can be easily accomplished with an Arduino board and a Bluetooth module that is easy to use.

To register the motion of the mouse, a GY-521 accelerometer can be used. Acceleration in 2 axes is measured to record the movement of the hand. In the original project, clicks were registered by the user bending their fingers. However, the implementation was complicated. I would suggest that to record clicks, pushbuttons can be placed on the index and middle fingers for left and right clicking respectively. The buttons should be pressed with your thumb to register a click. This is easier to implement. The data from the accelerometer and the pushbuttons should then be sent to the computer via the bluetooth module. Then, we need to write code in python to read this data and move the mouse based on it.

Advantages of this approach:- Cheap and easy to implement.
Disadvantages:- The python code will have to be running while the mouse is connected. Also, reading data from the bluetooth module in python might be tough.
