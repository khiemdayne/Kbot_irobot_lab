# Kbot_irobot_lab
KBot is an autonomous differential drive robot with two wheels. Its main processing unit is a Raspberry Pi 4 B running Ubuntu Mate 20.04 and the ROS 1 (ROS Noetic) middleware. This respository contains ROS driver packages, ROS Control Hardware Interface for the real robot and configurations for simulating DiffBot. The formatted documentation can be found at: https://ros-mobile-robots.com.

# Package Overview
kbot_base: ROS Control hardware interface including controller_manager control loop for the real robot. The scripts folder of this package contains the low-level base_controller that is running on the Teensy microcontroller.

kbot_bringup: Launch files to bring up the hardware drivers (camera, lidar, imu, ultrasonic, ...) for the real DiffBot robot.

kbot_control: Configurations for the diff_drive_controller of ROS Control used in Gazebo simulation and the real robot.

mobile_robot_v2 URDF description of KBot including its sensors.

kbot_gazebo: Simulation specific launch and configuration files for KBot

dkbot_msgs: Message definitions specific to KBot, for example the message for encoder data

kfbot_navigation: Navigation based on move_base package; launch and configuration files.

kbot_slam: Simultaneous localization and mapping using different implementations (e.g., gmapping) to create a map of the environment


# Hướng dẫn sử dụng:
Điều khiển robot với stering:
roslaunch kbot_gazebo kbot.launch

Quet map voi salm_gmapping: 
roslaunch kbot_gazebo kbot.launch
roslaunch kbot_slam kbot_slam.launch

Điều hướng:
roslaunch kbot_navigation kbot.launch
