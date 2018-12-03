RomeoMotor Library v1.04
12/3/2018

This library is intended to use the DFRobot Romeo BLE controller with robotics applications.


It was inspired by Carnegie Mellon's Robotics Academy's work on RobotC for the VEX Controls system.

RomeoMotor()
  
	A RomeoMotor object must be constructed using a parameter of 1 or 2, in order to indicate which motor M1 or M2 is used.



void move(int speed)
  
	The move() method takes in an integer value from -127 to +127 to make each motor move.

		-127 is maximum reverse

		0 is not moving

		+127 is maximum forward


	There is a dead range of +-20 where the motor won't move.


	If a value greater than +127 or less than -127 is passed in, then they will be reduced to 100 or -100.



void flip(boolean flip)

	The flip() method allows you to reverse all subsequent calls to the moveMotor() method.

	This is very useful for robot drivetrains that have motors facing in opposite direction.

	You can use the same speed values in move() to go forward, instead of turning.
  


void kill()

	The kill() method stops the motor from moving the rest of the program.
  The only way to regain functionality of the motor is to reset the Arduino.
  



