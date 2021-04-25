#                                                                        TURB'O'SKIM

# ABSTRACT
An oil spill is the release of liquid hydrocarbon into the environment especially in oceans and is a form of man made disasater. 35.7% of oil spilt in oceans is from oil tanker vessels. This hugely affects the marine ecosystem and also tourism, marine economy and the human health. Thus oil spill is a biological, economical and a social disasater. This project aims to detect the oil spilt from vessels accurately and also as early possible with the help of different sensors and mechanisms. This project not only stops at that but also makes use of an oil skimming that will be pressed into action as soon as oil spill is detected. An ESP8266 microcontroller, a GPS module and also wifi signals connected to an app interface to control the entire process.  This project is a true and unique solution that employs modern technologies like IoT as well as an app interface to detect and clean up the oil spilt making it highly stable, efficient and also economical. The bot which is used to clean up the oil spilt makes use of a driver module as well as belt based skimming mechanism to do it's job efficiently. We have designed this project to be controlled manually in case of any exegesis without much strain making the response without any time lag and making recovery as soon as possible.

# OVERVIEW
SMART OIL SKIMMER
1.FIRST IOT BASED OIL SKIMMER
2.USES GPS MODULE FOR NAVIGATION
3.L298n DRIVER MODULE FOR BOT MOVEMENT

# MATERIALS REQUIRED
1. Arduino ESP8266
2. 9V Batteries and 9V clips
3. Motor Drive Controller Module L298N
4. Ublox NEO 6M GPS Module
5. IRFZ44N N-Channel MOSFET
6. HX711 Module
7. Jumper Wires


# PROTOTYPE OF OUR BOT 
![image](https://user-images.githubusercontent.com/80695417/113501811-a3e66700-9545-11eb-912d-bcfac457899f.png)
![image](https://user-images.githubusercontent.com/80695417/113508595-972a3900-956e-11eb-85d3-68f361fac640.png)




# TinyGPSPlus
A new, customizable Arduino NMEA parsing library
A *NEW* Full-featured GPS/NMEA Parser for Arduino
TinyGPS++ is a new Arduino library for parsing NMEA data streams provided by GPS modules.

Like its predecessor, TinyGPS, this library provides compact and easy-to-use methods for extracting position, date, time, altitude, speed, and course from consumer GPS devices. 

However, TinyGPS++’s programmer interface is considerably simpler to use than TinyGPS, and the new library can extract arbitrary data from any of the myriad NMEA sentences out there, even proprietary ones.

See [Arduiniana - TinyGPS++](http://arduiniana.org/libraries/tinygpsplus/) for more detailed information on how to use TinyGPSPlus

![image](https://user-images.githubusercontent.com/80695417/113501846-d8f2b980-9545-11eb-940d-97ce94e2d93b.png)  ![image](https://user-images.githubusercontent.com/80695417/113508466-d0ae7480-956d-11eb-9f43-8e134b11ef57.png)





# HX711

Arduino library for HX711 24 bit ADC  used for load cells and scales.

# Description

This HX711 library has an interface which is a superset of a library made by bogde.
Some missing functions were added to get more info from the lib. 

Another important difference is that this library uses floats. The 23 bits mantisse 
of the IEE754 float matches the 24 bit ADC very well. Furthermore it gave a smaller
footprint. 

**Main flow**

First action is to call **begin(DATAPIN, CLOCKPIN)** to make connetion to the **HX711**.

Second step is callibration for which a number of functions exist.
* **tare()** measures zero point
* **set_scale(factor)** set a known conversion factor e.g. from EEPROM.
* **callibrate_scale(WEIGHT, TIMES)** determines the scale factor based upon a known weight e.g. 1 Kg.

Steps to take for callibration
1. clear the scale
1. call tare() to set the zero offset
1. put a known weight on the scale 
1. call callibrate_scale(weight) 
1. scale is calculated.
1. save the offset and scale for later use e.g. EEPROM.


**Pricing**

Some price functions were added to make it easy to use this library
for pricing goods or for educational purposes. These functions are under discussion
if they will stay. Another set of function to add weights together didn't make it in 
the 0.2.0 release, it is on a todo list.

For weight conversion functions see https://github.com/RobTillaart/weight

## Notes

**Scale values for loadcells**

These scale values worked pretty well with a set of loadcells, 
Use callibrate to find your values.

* 5 KG loadcell   scale.set_scale(420.52); 
* 20 KG loadcell  scale.set_scale(127.15); 

**Connections HX711**

A+/A-  uses gain of 128 or 64
B+/B-  uses gain of 32

# HX711 MODULE
![image](https://user-images.githubusercontent.com/80695417/113501894-3ab32380-9546-11eb-9aa5-8b218d3f2dc9.png)


# L298N

This L298N Motor Driver Module is a high power motor driver module for driving DC and Stepper Motors. This module consists of an L298 motor driver IC and a 78M05 5V regulator. L298N Module can control up to 4 DC motors, or 2 DC motors with directional and speed control.

# Description 
ENA & ENB pins are speed control pins for Motor A and Motor B while IN1& IN2 and IN3 & IN4 are direction control pins for Motor A and Motor B.

In order to have a complete control over DC motor, we have to control its speed and rotation direction. This can be achieved by combining these two techniques:-
PWM – For controlling speed
H-Bridge – For controlling rotation direction

Warning:
1.You can put the jumper in place, if the motor power supply is below 12V. If it is greater than 12V, you should remove the jumper to avoid the onboard 5V regulator from getting damaged.

2.Also DO NOT supply power to both the motor power supply input and 5V power supply input when jumper is in place.

# L298N MODULE
![image](https://user-images.githubusercontent.com/80695417/113501870-08092b00-9546-11eb-9424-3eba47a80759.png) ![image](https://user-images.githubusercontent.com/80695417/113508584-7cf05b00-956e-11eb-9985-91e9f1e784fb.png)
