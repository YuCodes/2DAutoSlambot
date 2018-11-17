# 2DAutoSlambot
2D Slam Bot , which uses skid steer drive, gmapping and amcl for mapping and navigation

you will need following dependancies to successfully run the launch files


sudo apt-get install ros-kinetic-diff-drive-controller
sudo apt-get install ros-kinetic-amcl
sudo apt-get install ros-kinetic-gmapping
sudo apt-get install ros-kinetic-navigation

After making the catkin package
you can launch the launch files given in the launch folder

roslaunch gslambot gmaprobot.launch model:=path to the /urdf/gmapbot.xacro file

if you want to move the robot using the keyboard you will want to run the following node
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
 
if you want the bot to use slam and navigate use these two files
roslaunch gslambot move_base.launch
you can add a camera to the rviz as well if you want the output image to be displayed in the rviz
 
