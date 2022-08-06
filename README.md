# Third-Task

# use turtlebot3 with SLAM approach to create and save map #


## First stage (go to this website https:/ /turtlebot3.robotis.com/)  ##
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
## 1- (Install TurtleBot3 Packages)  ##
Install TurtleBot3 via Debian Packages.

 ```
$ sudo apt install ros-noetic-dynamixel-sdk
$ sudo apt install ros-noetic-turtlebot3-msgs
$ sudo apt install ros-noetic-turtlebot

```
## 2- (Network Configuration)  ##
Connect PC to a WiFi device and find the assigned IP address with the command below.
 ```
1- $ ifconfig
2- then edting with your ip address my( 127.0.0.1)
3- Open the file and update the ROS IP settings with the command below.
$ nano ~/.bashrc
4- Press Ctrl+END or Alt+/ to move the cursor to the end of line.
Modify the address of localhost in the ROS_MASTER_URI and ROS_HOSTNAME with the IP address acquired from the above terminal window.
5- Source the bashrc with below command.
$ source ~/.bashrc

```
## Second stage (Navigation)  ##
 is to move the robot from one location to the specified destination in a given environment.
  ```
  1- If roscore is not running on the Remote PC, run roscore.
  2- If the Bringup is not running on the TurtleBot3 SBC, launch the Bringup. Skip this step if you have launched bringup previously.
Open a new terminal from Remote PC with Ctrl + Alt + T and connect to Raspberry Pi with its IP address. The default password is turtlebot. Please use the proper keyword among burger, waffle, waffle_pi for the TURTLEBOT3_MODEL parameter.
3-Launch the Navigation.
Please use the proper keyword among burger, waffle, waffle_pi for the TURTLEBOT3_MODEL parameter.
$ export TURTLEBOT3_MODEL=burger
$ roslaunch turtlebot3_navigation turtlebot3_navigation.launch map_file:=$HOME/map.yaml
  ```
  ![Screenshot from 2022-08-06 11-49-54](https://user-images.githubusercontent.com/108955178/183259139-69341753-a2de-4481-9ac7-bd73a34809f6.png)
![Screenshot from 2022-08-06 11-51-55](https://user-images.githubusercontent.com/108955178/183259148-192dae75-ed55-4944-8ff3-5ffcafa7e2c3.png)

  ## Third stage (Simulation)  ##
  This Gazebo Simulation uses ROS Gazebo package, therefore, proper Gazebo version for ROS1 Noetic has to be installed before running this instruction.

# Install Simulation Package
```
$ cd ~/catkin_ws/src/

$ git clone -b noetic-devel https://github.com/ROBOTIS-GIT/turtlebot3_simulations.git

$ cd ~/catkin_ws && catkin_make

```
# Install Simulation Package
Launch Simulation World
```
$ export TURTLEBOT3_MODEL=burger

$ roslaunch turtlebot3_gazebo turtlebot3_empty_world.launch
```
#  my work #
![Screenshot from 2022-08-06 10-29-41](https://user-images.githubusercontent.com/108955178/183259413-f1c18aa1-df11-48b3-a1a0-a6596323ab2a.png)





