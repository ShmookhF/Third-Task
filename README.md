# Third-Task
```
use turtlebot3 with SLAM approach to create and save map
```

## First (go to this website https:/ /turtlebot3.robotis.com/)  ##
 Then click on Quick Start Guide and Chose ros (noetic) from the top of the page
 ```
 last Write these code in terminal (Dependent ROS Packages)
 
 sudo apt-get install ros-noetic-joy ros-noetic-teleop-twist-joy \
  ros-noetic-teleop-twist-keyboard ros-noetic-laser-proc \
  ros-noetic-rgbd-launch ros-noetic-rosserial-arduino \
  ros-noetic-rosserial-python ros-noetic-rosserial-client \
  ros-noetic-rosserial-msgs ros-noetic-amcl ros-noetic-map-server \
  ros-noetic-move-base ros-noetic-urdf ros-noetic-xacro \
  ros-noetic-compressed-image-transport ros-noetic-rqt* ros-noetic-rviz \
  ros-noetic-gmapping ros-noetic-navigation ros-noetic-interactive-marker

```
## second (Install TurtleBot3 Packages)  ##
Install TurtleBot3 via Debian Packages.

 ```
$ sudo apt install ros-noetic-dynamixel-sdk
$ sudo apt install ros-noetic-turtlebot3-msgs
$ sudo apt install ros-noetic-turtlebot

```
## Third (Network Configuration)  ##
Connect PC to a WiFi device and find the assigned IP address with the command below.
 ```
$ ifconfig
ف

```
