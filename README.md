# RomeoMotor Library v1.06
12/7/2018

This library provides functions to control an Arduino robot using the DFRobot Romeo BLE board.
It was inspired by Carnegie Mellon's Robotics Academy's work on RobotC for the VEX Controls system.


# RomeoMotor()
### description:
* A RomeoMotor object must be constructed to use one of the two motor ports provided on the DFRobot Romeo board.
### syntax:
```c
RomeoMotor motorName(motor)
```
### parameters:
* motor - ```1``` or ```2```, the number of the motor used, corresponding to M1 or M2 on the Romeo board.


# move()
### description:
* Makes the motor move a particular speed and direction.
* There is a dead range of +-20 where the motor won't move.
* If a value greater than +127 or less than -127 is passed in, then they will be reduced to 100 or -100.
### syntax:
```c
move(speed)
```
### parameters:
* speed - an integer from -127 to +127 to make the motor move
  * ```127``` is maximum reverse
  * ```0``` is not moving
  * ```-127``` is minimum forward
### returns:
* none


# flip()
### description:
* The flip() method allows you to reverse all subsequent calls to the moveMotor() method.
* This is very useful for robot drivetrains that have motors facing in opposite direction.
* You can use the same speed values in move() to go forward, instead of turning.
### syntax:
```c
flip(isFlipped)
```
### parameters:
* isFlipped - ```true``` or ```false```
### returns:
 * none
 
 
# shutDown()
### description:
* The shutDown() method stops the motor from moving the rest of the program.
* The only way to regain functionality of the motor is to reset the Arduino.
### syntax:
```c
shutDown()
```
 ### parameters:
 * none
 ### returns:
 * none

 
