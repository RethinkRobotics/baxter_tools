cmake_minimum_required(VERSION 3.0.5)
project(baxter_tools)

find_package(catkin
  REQUIRED
  COMPONENTS
  rospy
  sensor_msgs
  geometry_msgs
  cv_bridge
  baxter_interface
  baxter_core_msgs
  baxter_maintenance_msgs
)

catkin_python_setup()

catkin_package(
  CATKIN_DEPENDS
  rospy
  sensor_msgs
  geometry_msgs
  cv_bridge
  baxter_interface
  baxter_core_msgs
  baxter_maintenance_msgs
)

catkin_install_python(PROGRAMS 
    scripts/calibrate_arm.py
    scripts/camera_control.py
    scripts/enable_robot.py 
    scripts/smoke_test.py
    scripts/tare.py
    scripts/tuck_arms.py
    scripts/update_robot.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
  )
# install(
#   DIRECTORY scripts/
#   DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#   USE_SOURCE_PERMISSIONS
# )

install(
  DIRECTORY share/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/share
  USE_SOURCE_PERMISSIONS
)
