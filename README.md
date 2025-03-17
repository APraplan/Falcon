# Falcon
Falcon 6DoF robotic arm

# Intro
This project aim to design a 6 DoF desktop size robotic arm. The robotic arm should have a payload capacity of 500g for a range of 40cm. This arm will be actuated by stepper motors controlled by a raspberry pico RP2040 and 6 TMC 2209 stepper drivers. The end-stops should be inductive sensors. The high level path planning and inverse kynematic will be implemented using ROS MoveIt on a Raspberry Pi 5. 

# CAD design
## Wrist
The wrist has tow DoF, with one stepper and a 1/10 reduction gearbox and a second stepper with a 1/5 belt reduction. The wrist also has pneumatic interfaces for the end effector tooling.

<p align="center">
  <img src="https://github.com/user-attachments/assets/ead99be1-a92c-4ae3-b20c-9e6af9c13cc3" width="45%">
  <img src="https://github.com/user-attachments/assets/b5577282-a4bd-4770-a3fd-5082dee8f8ee" width="45%">
</p>

## Elbow
The elbow has one Nema 17 stepper motor with a 1/10 belt reduction.

<p align="center">
  <img src="https://github.com/user-attachments/assets/b94808da-95bc-4add-8444-34c701f552e5" width="45%">
  <img src="https://github.com/user-attachments/assets/edb2539b-d091-427e-b09d-57892dfa820c" width="45%">
</p>

## Arm
The arm has no stepper motors on it. All the stepper motor Nema 17 are in the base. The torque transmission is made using HDT3 belts with a reduction of 1/20.

<p align="center">
  <img src="https://github.com/user-attachments/assets/785417e9-195e-4a62-8fee-304d10841a2a" width="45%">
  <img src="https://github.com/user-attachments/assets/36cdadef-85e5-40c4-bdca-d8ab4c70dab5" width="45%">
</p>

## Base
The base has three stepper motors to control the rotation and the movement of the amr and elbow. Moreover, all the control electornic, stepper driver and brain are integrated in the base with a cooling fan and a safety stop switch.

<p align="center">
  <img src="https://github.com/user-attachments/assets/a33a7798-c6bf-4f97-8140-2cf0c18f96a1" width="45%">
  <img src="https://github.com/user-attachments/assets/99a18b82-c3cd-4fb0-90e5-0c794de07a4b" width="45%">
</p>

## Assembly

![Assembly](https://github.com/user-attachments/assets/27752df1-5d13-49bd-a8c6-f987aa9fc1a4)

<p align="center">
  <img src="https://github.com/user-attachments/assets/47bf1dfd-0fbc-49b7-afae-a92c3d3cd7f7" width="45%">
  <img src="https://github.com/user-attachments/assets/6fd15e36-f6bf-4934-b4c9-65d59c3acaae" width="45%">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/4bd7a003-6499-408a-8bbc-bd1ec8580b8f" width="45%">
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/0a944c2f-2ab9-40e5-8ef8-a081c59161f2" width="45%">
  <img src="https://github.com/user-attachments/assets/57deade5-581f-4ee4-921a-f08c3a05ea98" width="45%">
</p>

# PCB design
A PCB has been designed to interface 6 BTT TMC2209 stepper drivers with a Raspberry Pico and provide 5v for all the  control electornic.

## Schematics
The schematics are visible here with the MCU integration, the Power distribution for the DCDC up to 24V to 5v, the IO for the gestion of the sensors and the Drivers interfaces and connections.

<p align="center">
  <img src="https://github.com/user-attachments/assets/07e0b386-99da-4770-870f-a09427635adc" width="45%">
  <img src="https://github.com/user-attachments/assets/ddc91d50-57e8-4951-8452-649ee695e448" width="45%">
</p>
<p align="center">
  <img src="https://github.com/user-attachments/assets/6fa0fed9-4eb1-4709-89a4-85571006537b" width="45%">
  <img src="https://github.com/user-attachments/assets/af8ade21-6b91-4de1-aa42-2afbb6bd6147" width="45%">
</p>


## PCB layout
The layout of the PCB has been realized to follow the form factor of a raspberry pi for an easy integration. The result is very compact on a 4 layer PCB.

![PCB_no silk](https://github.com/user-attachments/assets/b1e554ed-7127-44df-9de9-1357e8321172)
![PCB_3d](https://github.com/user-attachments/assets/a7970abd-f36c-4124-98ed-1d74840b06dd)

## PCB testing and validation
The PCB has been ordered through PCBway with the assembly. The divers and the Raspberry Pico inrefaces seamlessly. All the functionnalities have been tested, the PCB can handle the stress test and only two small design errors due to component footprint errors have been encountered ans will be corrected in the next board revision.

![erasebg-transformed(1)](https://github.com/user-attachments/assets/cdcf8442-818d-4407-b90a-dff25ecf5d4f)

<p align="center">
  <img src="https://github.com/user-attachments/assets/96c695ed-8eeb-4e8a-b3be-1987135347cc" width="45%">
  <img src="https://github.com/user-attachments/assets/680e20f6-b872-445d-8456-30e5995e3116" width="45%">
</p>

# Components
Bearings, steppers, sensors, plastic parts descriptions...

# Assembly
Images of the assembly ...

# Software
## Embeded software and communication
## ROS MoveIt
## Webapp
