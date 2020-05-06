# Elec_Club_MiniTask2
# 1. Smart Glove Computer Mouse
## Problem Statement:-
A smart glove that functions as a mouse which you can control by moving your hand in the air.

## Ideation:- 
Currently, the project makes use of a Binho Qwiic Interface board and a Qwiic accelerometer. However, I think that this is unnecessarily complicated and that this can be easily accomplished with an Arduino board and a Bluetooth module that is easy to use.

To register the motion of the mouse, a GY-521 accelerometer can be used. Acceleration in 2 axes is measured to record the movement of the hand. In the original project, clicks were registered by the user bending their fingers. However, the implementation was complicated. I would suggest that to record clicks, pushbuttons can be placed on the index and middle fingers for left and right clicking respectively. The buttons should be pressed with your thumb to register a click. This is easier to implement. The data from the accelerometer and the pushbuttons should then be sent to the computer via the bluetooth module. Then, we need to write code in python to read this data and move the mouse based on it.

Advantages of this approach:- Cheap and easy to implement.

Disadvantages:- The python code will have to be running while the mouse is connected. Also, reading data from the bluetooth module in python might be tough.

# 2. Arduino Anti-dog Trash Can
## Problem statement:-
A trash can that ensures that a dog doesn't take trash from it.

## Ideation:-
Currently, the project makes use of a button to check if the trash can is open for more than 5 seconds and if it is, it plays an audio to make the dog go away. However, the disadvantage of this is that it can mistake the owner for the dog.

I suggest using two IR proximity sensors to check if the dog is trying to open the can. One should be be near the top of the can and the other should be near the bottom. Both of them should be opposite to the hinge of the lid. The states of these two sensors can be compared to find out if it is a dog or a human near the can. If it is only the bottom one that is trigerred then it is a dog but if it is a human both will be trigerred. If the dog tries to trick the senosors by standing on the side, then only the top sensor will get trigerred when it tries to open it. The data from the sensors will be sent to an Arduino Uno which will play the audio if the required conditions are satisfied.

Advantages of this approach:- Will be able to distinguish between human and dog.

Disadvantages:- Will be tougher to implement. 
