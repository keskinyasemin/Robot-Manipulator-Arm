# Robot-Manipulator-Arm
Robot manipulator arm with RViz and Gazebo

The term project for Robotics course. Robotic model is created in my_robot.urdf file. Katana robot manipulator arm mesh is implemented to first two links for better visual apperance.

#### Dependencies:
- Ubuntu 18.04.6 LTS (Bionic Beaver)
- ROS Melodic Morenia

## How to Run
1. First, install catkin as mentioned in ros wiki https://wiki.ros.org/catkin

```
$ sudo apt-get install cmake python-catkin-pkg python-empy python-nose python-setuptools libgtest-dev build-essential
```
2. Then create a workspace for catkin https://wiki.ros.org/catkin/Tutorials/create_a_workspace

```
$ source /opt/ros/melodic/setup.bash
$ mkdir -p ~/catkin_ws/src
$ cd ~/catkin_ws/
$ catkin_make
$ source devel/setup.bash
```
3. Check if the path is accurate:
```
$ echo $ROS_PACKAGE_PATH
/home/youruser/catkin_ws/src:/opt/ros/kinetic/share
```
4. Copy mrobot folder to src folder in catkin_ws
5. Build the workspace for mrobot:
```
~catkin_ws$ catkin_make
~catkin_ws$ source ~/catkin_ws/devel/setup.bash
```
6. Run RViz. Open the config file (mrobot_rviz.rviz) that can be found in config folder. You need to install joint_state_publisher if prompted.:
```
$ roslaunch mrobot rviz.launch
```
7. Run Gazebo:
```
$ roslaunch mrobot mrobot.launch
```

### The Demonstration:

With the joint_state_publisher window we can change the degrees and positions for the joints.

![gif of rviz robot](/images/rviz_robot_manipulator.gif)

In Gazebo we can apply forces to links and see the robots' motion.

![gif of rviz robot](/images/gazebo_robot.gif)
