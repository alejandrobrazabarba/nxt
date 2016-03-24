ROSpberryNXT
============

Modified NXT and related ROS-Groovy Stacks for raspberry

Installation instructions:

cd  
mkdir rosbuild_ws  
cd rosbuild_ws/  
rosws init . /opt/ros/indigo/  
source setup.bash  
echo "export ROS_PACKAGE_PATH=~/rosbuild_ws/:$ROS_PACKAGE_PATH" >> ~/.bashrc  
source ~/.bashrc  
git clone https://github.com/alejandrobrazabarba/nxt.git && git clone https://github.com/alejandrobrazabarba/nxt_apps.git && git clone https://github.com/alejandrobrazabarba/nxt_robots.git  
rosdep install -y nxt_robots && rosdep install -y nxt_apps && rosdep install -y nxt  
rosmake -aivr #assisted_teleop and nxt_rviz_plugin will fail.  
roslaunch nxt_robot_sensor_car robot.launch  
