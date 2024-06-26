cmake_minimum_required(VERSION 3.0.2)
project(unitree_legged_msgs)

## Compile as C++11, supported in ROS Kinetic and newer
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  message_generation
  message_runtime
  roscpp
  rospy
)

# Message file
add_message_files(
  DIRECTORY
    msg
  FILES
    MotorCmd.msg
    MotorState.msg
    BmsCmd.msg
    BmsState.msg
    Cartesian.msg
    IMU.msg
    LED.msg
    LowCmd.msg
    LowState.msg
    HighCmd.msg
    HighState.msg
)

generate_messages()

catkin_package(
  CATKIN_DEPENDS
    message_runtime
)