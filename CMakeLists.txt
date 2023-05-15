cmake_minimum_required(VERSION 3.5.1)

project(trikey_gazebo)

find_package(catkin REQUIRED COMPONENTS
  gazebo_ros
  gazebo_plugins
  gazebo_ros_control
  roscpp
  rospy
  std_msgs
  rviz
  trikey_description
  trikey_control
  nav_msgs
  std_msgs
  tf2
)


catkin_package(
        CATKIN_DEPENDS
        gazebo_plugins
        message_runtime 
        std_msgs
        nav_msgs

)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)


## Mark executable scripts (Python etc.) for installation
## in contrast to setup.py, you can choose the destination
#catkin_install_python(PROGRAMS
#  scripts/odom
#  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#)


install(DIRECTORY launch
        DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

# install(DIRECTORY worlds
        # DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})