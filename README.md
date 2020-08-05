# common_rovers_application

## Required packages
1. common_arduino_application
2. common_camera_application
3. turtlebot3
4. urg_node **or** rplidar

**IMPORTANT**

[MASTER] : 172.20.10.3 : pi

[ROVERS 1] : 172.20.10.5 : mate-pi

[ROVERS 2] : 172.20.10.9 : mate-pi2

# Initialization
1. roscore [MASTER PC]
2. bringup_rovers_[ROVERS_NO]
	1. [MOTOR CONTROL]
		1. roslaunch common_arduino_application robot1_motor_control.launch [ROVERS 1]
		2. roslaunch common_arduino_application robot2_motor_control.launch [ROVERS 2]
		
	2. [CAMERA]
		1. roslaunch common_camera_application camera_robot1.launch [ROVERS 1]
		2. roslaunch common_camera_application camera_robot2.launch [ROVERS 2]
		
	3. [LIDAR]
		1. roslaunch common_rovers_application hokuyo_robot1.launch [ROVERS 1]
		2. roslaunch common_rovers_application hokuyo_robot2.launch [ROVERS 2]
	
## Camera Preview
1. roslaunch common_camera_application camera_robot1.launch [YOUR PC]

## Tele-Operation
1. roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch [YOUR PC]
