3D Navigation with TurtleBot3 Burger

This repository contains the code, launch files, and documentation for our capstone project using the TurtleBot3 Burger mobile robot. The robot performs 3D mapping, sensor fusion, SLAM, and autonomous navigation in an indoor environment. The project combines data from a LiDAR, depth camera (e.g., RealSense or OAK-D Pro), and IMU to produce an accurate 3D map and perform robust navigation.
📌 Project Overview

Autonomous mobile robots are widely used in industrial, research, and service applications. In this project, we built a pipeline to allow the TurtleBot3 Burger to:

    Fuse data from LiDAR, depth camera, and IMU.

    Generate 3D point cloud maps using RTAB-Map.

    Localize itself and perform SLAM in a previously unknown environment.

    Plan paths and autonomously navigate through complex indoor spaces.

Our system is developed using ROS Noetic on Ubuntu 20.04, and the simulation environment uses Gazebo for testing before deploying to the real robot.
📂 Repository Structure
turtlebot3_3d_navigation/
├── launch/                  # Launch files to start SLAM, sensor fusion, and navigation
├── src/                     # Custom nodes for sensor fusion and navigation
├── config/                  # Config files for robot_localization, RTAB-Map, etc.
├── worlds/                  # Custom Gazebo world files
├── models/                  # 3D models for simulation
├── maps/                    # Saved map and trajectory data
├── README.md                # You're here!

🚀 How to Use
✅ Prerequisites

    ROS Noetic (Ubuntu 20.04)

    TurtleBot3 packages

    RTAB-Map ROS

    RealSense SDK or OAK-D ROS driver

    robot_localization

    OpenCV and Open3D (for visualization)


    🧰 Installation

mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
git clone https://github.com/your-username/turtlebot3_3d_navigation.git
cd ..
catkin_make
source devel/setup.bash

    Tip: Ensure TURTLEBOT3_MODEL=burger is set in your .bashrc.
