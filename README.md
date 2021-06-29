# Turtlebot3 - gazebo & SLAM


* Install :
  1. Install Dependent ROS 1 Packages
    - $ sudo apt-get install ros-melodic-joy ros-melodic-teleop-twist-joy
    - $ sudo apt-get install ros-melodic-teleop-twist-keyboard ros-melodic-laser-proc
    - $ sudo apt-get instal ros-melodic-rgbd-launch ros-melodic-depthimage-to-laserscan
    - $ sudo apt-get instal ros-melodic-rosserial-arduino ros-melodic-rosserial-python
    - $ sudo apt-get instal ros-melodic-rosserial-server ros-melodic-rosserial-client
    - $ sudo apt-get instal ros-melodic-rosserial-msgs ros-melodic-amcl ros-melodic-map-server
    - $ sudo apt-get instal ros-melodic-move-base ros-melodic-urdf ros-melodic-xacro
    - $ sudo apt-get instal ros-melodic-compressed-image-transport ros-melodic-rqt*
    - $ sudo apt-get instal ros-melodic-gmapping ros-melodic-navigation ros-melodic-interactive-markers
  2. Install TurtleBot3 Packages
    - $ sudo apt-get install ros-melodic-dynamixel-sdk
    - $ sudo apt-get install ros-melodic-turtlebot3-msgs
    - $ sudo apt-get install ros-melodic-turtlebot3


* Launch :
  1. Launch Simulation World
    - $ export TURTLEBOT3_MODEL=burger
    - $ roslaunch turtlebot3_gazebo turtlebot3_world.launch
  2. Run SLAM Node
    - $ export TURTLEBOT3_MODEL=burger
    - $ roslaunch turtlebot3_slam turtlebot3_slam.launch slam_methods:=gmapping
  3. Run Teleoperation Node
    - $ export TURTLEBOT3_MODEL=burger
    - $ roslaunch turtlebot3_teleop turtlebot3_teleop_key.launch
  4. Save Map
    - $ rosrun map_server map_saver -f ~/map

<img src="map2.png"/>


## Faced Problems : 
  I faced a problem to run the gazebo and I fixed it by using this command : 
  - $ echo "export SVGA_VGPU10=0" >> ~/.bashrc
  - $ source ~/.bashrc
  
