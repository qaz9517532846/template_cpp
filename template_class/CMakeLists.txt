cmake_minimum_required(VERSION 3.0.2)
project(template_class)

add_compile_options(-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  roscpp
)

catkin_package(
   INCLUDE_DIRS include
#  LIBRARIES template_class
#  CATKIN_DEPENDS roscpp
#  DEPENDS system_lib
)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(template_class src/template_class.cpp)
target_link_libraries(template_class ${catkin_LIBRARIES})