# Turtlebot3



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
