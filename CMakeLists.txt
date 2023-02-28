cmake_minimum_required(VERSION 3.0.2)
project(otomo-camera)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  rospy
  sensor_msgs
)

catkin_package()

install(
  PROGRAMS
  scripts/cam
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(
  DIRECTORY
    launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
