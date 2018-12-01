# 2D Autonomous Slam Rover
2D Slam Bot , which uses skid steer drive, gmapping and adaptive monte carlo localization for mapping and navigation

you will need following dependancies to successfully run the launch files


sudo apt-get install ros-kinetic-diff-drive-controller\
sudo apt-get install ros-kinetic-amcl\
sudo apt-get install ros-kinetic-gmapping\
sudo apt-get install ros-kinetic-navigation

//create a catkin_workspace

mkdir -p 2DAutoSlambot/src\
cd 2DAutoSlambot\
catkin_make\
cd src\
catkin_create pkg gslambot\
cd gslambot

//After making the catkin package you can clone this repo inside the package.\
git clone  https://github.com/YuCodes/2DAutoSlambot/edit/master/README.md \
catkin_make

//To source your workspace folder if you haven't added in bashrc\
source devel/setup.bash 

you can launch the launch files given in the launch folder\
roslaunch gslambot gmaprobot.launch model:=path to the /urdf/gmapbot.xacro file

If you want to move the robot using the keyboard .. you will want to run the following node\
rosrun teleop_twist_keyboard teleop_twist_keyboard.py
 
if you want the bot to use slam and navigate use these two files\
roslaunch gslambot move_base.launch

you can add a camera to the rviz as well if you want the output image to be displayed in the rviz
 
<a href="https://imgflip.com/gif/2nx2yh"><img src="https://i.imgflip.com/2nx2yh.gif" title="made at imgflip.com"/></a>
