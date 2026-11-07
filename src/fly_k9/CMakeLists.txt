cmake_minimum_required(VERSION 3.8)
project(fly_k9)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)

add_executable(fly_k9_node src/fly_k9_node.cpp)
target_compile_features(fly_k9_node PUBLIC cxx_std_17)
ament_target_dependencies(fly_k9_node rclcpp)

install(TARGETS fly_k9_node
  DESTINATION lib/${PROJECT_NAME}
)

ament_package()
