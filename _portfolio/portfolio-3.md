---
title: "Eccentric Cycloid Actuator"
excerpt: " Fully 3D printed actuator with PD position control <br/><img src='/images/cycloid_act_1.png'>"
collection: portfolio
---

This actuator was fully 3D printed in PETG, and employs an eccentric cycloid drive, which is ideal for 3D printed parts as it relies on rolling of parts on one another. The actuator is driven by an RS775 DC motor, and a Cytron motor driver. Here is an image of the assembled actuator.

<img src="/images/cycloid_act_2.png" alt="actuator img" width="500"/>

PD control was implemented on an STM32F01 microcontroller to control the actuator. A magnetic encoder (AS5600) was used for angular rotation measurements. Data was collected via I2C.

The actuator shows fast response and can hold a torque of 2 N-m. [This video](https://drive.google.com/file/d/1Cs8KGymeBFPmqgqbfhwulbpNSIAqxEOw/view?usp=drive_link) shows the PD control in action as the actuator performs a full rotation back and forth. You can also look at the [actuator recovering from external torque](https://drive.google.com/file/d/1Cuh3Fh3aBVm5CJM1MXbTN35Ed5BCSAHX/view?usp=drive_link)

For this project, I had made an Arduino library to easily control multiple actuators together with Cytron type motor drivers (you will need an I2C multiplexer as well if you want to control more than one actuator). Feel free to check my github for the code.