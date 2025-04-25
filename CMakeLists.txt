cmake_minimum_required(VERSION 3.5)
project(nexus_4wd_mecanum_description)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(robot_state_publisher REQUIRED)
find_package(urdf REQUIRED)

include_directories(
  include
 ${rclcpp_INCLUDE_DIRS}
)

install(
  DIRECTORY urdf launch meshes params rviz worlds
  DESTINATION share/${PROJECT_NAME}
)

ament_export_dependencies(
  rclcpp
  robot_state_publisher
  urdf
)

ament_package()
