# Brisk-Helmet-and-Light-Control-System

The project can prevent riders from riding without wearing a helmet. The additional facilities provided together with this system increases the safety of the user. The smart control of headlamps adopted here gets activated when conditions satisfy. With this system, a safe two-wheeler journey is possible which would decrease the head injuries that occur from accidents caused by the absence of a helmet and additionally reduce the accident rate due to drunken driving and blurred vision.

# Block Diagram
Product consists of two sections a helmet section and a bike section
![1](https://user-images.githubusercontent.com/91025454/193393733-a3f51688-6eda-496c-96c3-533bc3a741f4.JPG)
![2](https://user-images.githubusercontent.com/91025454/193393735-62213927-3cd4-48bc-9f66-7a70cffacd5a.JPG)

# Results
The output of the project is shown in a prototype. The several stages of the programming is shown below with help of the serial monitor on Arduino IDE software.
![3](https://user-images.githubusercontent.com/91025454/193393864-a097f83a-04fb-4a9b-83a8-8b4fa56c9ec2.JPG)
We know that the helmet contains a snap/Roll switch for the presence of helmet. The program is written in such a way that there is no useful output when switch is inactive which means there is no output in the Normally Open pin of the switch which is connected in series with a Resistor (100Ω) to one of the digital pins. A Serial.println command is used to give a visual feed of the above mentioned state.
![4](https://user-images.githubusercontent.com/91025454/193393889-7321170c-72b7-4fe3-a4c8-73616d540e5b.JPG)
When the rider wears the helmet the switch is activated so the program now goes to the second choice which is alcohol detection using the Mq3 gas sensor module interfaced with the microcontroller board. The sensor checks for alcohol content, if detected does nothing, but for the sake visual acknowledgment we use Serial.println command to show a piece of string.
![5](https://user-images.githubusercontent.com/91025454/193393914-f50768d2-9324-4451-89bc-2874ce71d51f.JPG)
When the head is detected i.e when the rider wears the helmet switch gets pressed microcontroller gets a high value and after that the mq3 comes into action and checks for alcohol when there is no alcohol the output will be the values that is mapped in the program from the gyroscope. The serial monitor window shows the values mapped from the gyroscope.
![6](https://user-images.githubusercontent.com/91025454/193393938-b9720d00-7a51-4066-85d1-83d562ea3e50.JPG)
The bike section receives the gyro values from the master Bluetooth module. The receiver section is programmed in a way that when it receives the values the ignition gets ON and also the received values is used to control the servo motor.
