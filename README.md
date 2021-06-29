# Turtlebot3 - gazebo & SLAM


* Install :
  1. Install Dependent ROS 1 Packages
    - $ sudo apt-get install ros-kinetic-joy ros-kinetic-teleop-twist-joy \
        ros-kinetic-teleop-twist-keyboard ros-kinetic-laser-proc \
        ros-kinetic-rgbd-launch ros-kinetic-depthimage-to-laserscan \
        ros-kinetic-rosserial-arduino ros-kinetic-rosserial-python \
        ros-kinetic-rosserial-server ros-kinetic-rosserial-client \
        ros-kinetic-rosserial-msgs ros-kinetic-amcl ros-kinetic-map-server \
        ros-kinetic-move-base ros-kinetic-urdf ros-kinetic-xacro \
        ros-kinetic-compressed-image-transport ros-kinetic-rqt* \
        ros-kinetic-gmapping ros-kinetic-navigation ros-kinetic-interactive-markers
  2. Install TurtleBot3 Packages
    - $ sudo apt-get install ros-kinetic-dynamixel-sdk
    - $ sudo apt-get install ros-kinetic-turtlebot3-msgs
    - $ sudo apt-get install ros-kinetic-turtlebot3


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

<img src="map2.pgm"/>


## Faced Problems : 
  I faced a problem to run the gazebo and I fixed it by using this command : 
  - $ echo "export SVGA_VGPU10=0" >> ~/.bashrc
  - $ source ~/.bashrc
  
