cmake_minimum_required(VERSION 2.8.3)
project(ocv_msgs)

find_package(catkin REQUIRED COMPONENTS std_msgs geometry_msgs message_generation 
)

add_message_files(
  FILES
  ocv.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  geometry_msgs
)

catkin_package(
  INCLUDE_DIRS
  LIBRARIES 
  CATKIN_DEPENDS message_runtime
  DEPENDS
)
