# Peristaltic-Pump
## Description / Used Hardware
Aim of the project is a DIY version of a peristaltic Pump. Control of mass flow is done with a rotary Potentiometer and an ESP32. The used motor to drive the pump is a 28byj-48 5V Motor with an Uln2003 Driver board. For compression of the hose three grooved ball bearings ( innerdiameter = 8 mm, outerdiameter = 22mm, height/thickness = 7mm) ) are used.

## 3D-printed Parts

* Casing with place for pump 
* 3D Model of 28byj-48 5V Motor (just used for design)
* Moving parts mounted on the motor-axis (holding bearings)

## Code Snippet
* Code for steering the 28BYJ-48
```
import Stepper
from machine import Pin
s1 = Stepper.create(Pin(16,Pin.OUT),Pin(17,Pin.OUT),Pin(5,Pin.OUT),Pin(18,Pin.OUT), delay=1)
s1.step(100)
s1.step(100,-1)
s1.angle(180)
s1.angle(360,-1)
```

## TODO

* Test other motor
* Redesign 3D
* Printing and Testing

## DONE
* print parts 
* write control-code
* testing and adaption (The 28BYJ-48 Motor has not enough torque)


## Sources

The code for the stepper driver was taken from https://github.com/zhcong/ULN2003-for-ESP32
