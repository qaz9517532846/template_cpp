cmake_minimum_required(VERSION 3.0.2)
project(template_cpp)

add_compile_options(-std=c++17)

find_package(catkin REQUIRED COMPONENTS
  roscpp
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES template_cpp
#  CATKIN_DEPENDS roscpp
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(template_ex1 src/template_ex1.cpp)
target_link_libraries(template_ex1 ${catkin_LIBRARIES})

add_executable(template_ex2 src/template_ex2.cpp)
target_link_libraries(template_ex2 ${catkin_LIBRARIES})

add_executable(template_ex3 src/template_ex3.cpp)
target_link_libraries(template_ex3 ${catkin_LIBRARIES})

add_executable(template_ex4 src/template_ex4.cpp)
target_link_libraries(template_ex4 ${catkin_LIBRARIES})

add_executable(template_ex5 src/template_ex5.cpp)
target_link_libraries(template_ex4 ${catkin_LIBRARIES})