# Kbot_irobot_lab
KBot is an autonomous 2wd differential drive robot using ROS Noetic on a Raspberry Pi 4 B. With its SLAMTEC Lidar and the ROS Control hardware interface it's capable of navigating in an environment using the ROS Navigation stack and making use of SLAM algorithms to create maps of unknown environments.
KBot is an autonomous differential drive robot with two wheels. Its main processing unit is a Raspberry Pi 4 B running Ubuntu Mate 20.04 and the ROS 1 (ROS Noetic) middleware. This respository contains ROS driver packages, ROS Control Hardware Interface for the real robot and configurations for simulating DiffBot. The formatted documentation can be found at: https://ros-mobile-robots.com.
# Package Overview
kbot_base: ROS Control hardware interface including controller_manager control loop for the real robot. The scripts folder of this package contains the low-level base_controller that is running on the Teensy microcontroller.
kbot_bringup: Launch files to bring up the hardware drivers (camera, lidar, imu, ultrasonic, ...) for the real DiffBot robot.
kbot_control: Configurations for the diff_drive_controller of ROS Control used in Gazebo simulation and the real robot.
kbot_description: URDF description of DiffBot including its sensors.
kbot_gazebo: Simulation specific launch and configuration files for DiffBot.
dkbot_msgs: Message definitions specific to DiffBot, for example the message for encoder data.
kfbot_navigation: Navigation based on move_base package; launch and configuration files.
kbot_slam: Simultaneous localization and mapping using different implementations (e.g., gmapping) to create a map of the environment
