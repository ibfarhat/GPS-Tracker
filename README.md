# Project Introduction

This is a GPS tracker board that periodically checks the GPS coordinates and sends them to a predefined remote server on the internet.

![](https://github.com/mohamedboubaker/GPS-Tracker/blob/main/Media/PCB.JPG)
*Figure 1. Manufactured PCB*





The idea is basically a microcontroller, STM32F030, that periodically sends AT commands via UART to the SIM808 GPS/GPRS module to get GPS data and then sends these data to a Mosquitto MQTT server hosted on an AWS EC2. This data gets also encrypted with AES-128 in Electronic Code Book (ECB) mode before being sent to the server. AES algorithm was implemented from scratch for learning purposes. (Note: In a production application, it's better to use a known AES implementations. Example: WolfSSL)

The power input of the circuit is regulated using a DC-DC down converter Texas Instruments TPS5430DDA with input voltage ranging from 5.5V to 36V 

## Circuit diagram  and PCB
Above is a picture of the manufactured PCB. The front side is on the left and contains mainly the TPS5430DDA Power regulation circuit on top and the STM32F0 in the center. On the right you see the PCB's backside which contains the SIM808 and SIM card holder circuit.

![alt text](https://github.com/mohamedboubaker/GPS-Tracker/blob/main/Media/circuit_diagram.jpg)
*Figure 2. Circuit Diagram*

## PCB Layout 
![alt text](https://github.com/mohamedboubaker/GPS-Tracker/blob/main/Media/Layout_FrontAndBack.png)
*Figure 3. Layout: front side on the left, back side on the right*

## PCB 3D Model
![](https://github.com/mohamedboubaker/GPS-Tracker/blob/main/Media/3D_FrontAndBack.png)
*Figure 4. 3D Model of the PCB*
