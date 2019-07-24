Laikago working with ROS. The test environment is: Ubuntu 16.04 + ROS Kinetic.

# Instructions:
## Build:
* `cd ~/path-to-catkin-workspace`  (for example, replace 'path-to-catkin-workspace' with 'catkin_ws')
* `catkin_make`
* `source ~/path-to-catkin-workspace/devel/setup.bash`

### laikago_controller:
This ros-type controller allow user control joints with position, velocity and torque.

### laikago_msgs:
ros-type message, including command and state of high-level and low-level control.
It would be better if it be compiled firstly, otherwise you may have dependency problems (such as that you can't find the header file).

### laikago_description:
including mesh, urdf and xacro files of laikago.

### laikago_gazebo:
Gazebo8 is recommended. It is not compatible with other versions like Gazebo7.
Make sure unders have been installed:
```
sudo apt-get install ros-kinetic-controller-manager ros-kinetic-ros-control ros-kinetic-ros-controllers ros-kinetic-joint-state-controller ros-kinetic-effort-controllers ros-kinetic-velocity-controllers ros-kinetic-position-controllers ros-kinetic-robot-controllers ros-kinetic-robot-state-publisher ros-kinetic-gazebo8-ros ros-kinetic-gazebo8-ros-control ros-kinetic-gazebo8-ros-pkgs ros-kinetic-gazebo8-ros-dev
```

run with:
* `roslaunch laikago_description laikago_rviz.launch`
The robot should be spawned in Rviz.
