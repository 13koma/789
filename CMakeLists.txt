cmake_minimum_required(VERSION 3.8)
project(dh_gripper_driver)

find_package(ament_cmake REQUIRED)

# Install Python module
install(DIRECTORY dh_gripper_driver/
  DESTINATION lib/python3/dist-packages/dh_gripper_driver
)

# Install Python scripts
install(PROGRAMS
  scripts/gripper_node.py
  scripts/test_gripper_cli.py
  scripts/test_gripper_ros2.py
  DESTINATION lib/${PROJECT_NAME}
)

# Install config
install(DIRECTORY config/
  DESTINATION share/${PROJECT_NAME}/config
)

# Install launch
install(DIRECTORY launch/
  DESTINATION share/${PROJECT_NAME}/launch
)

ament_package()
