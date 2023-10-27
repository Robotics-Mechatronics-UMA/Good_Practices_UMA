cmake_minimum_required(VERSION 2.8.3)
project(ros_cpp_template)

add_compile_options(-std=c++11)

set(${PROJECT_NAME}_DEPENDS
  #Package dependencies
  roscpp
  std_msgs
)
    
set(${PROJECT_NAME}_INCLUDE_DIRS
  #Include folders
  include
)

find_package(catkin REQUIRED COMPONENTS
  ${${PROJECT_NAME}_DEPENDS}
)

#What to export (include dirs, libraries, etc)
catkin_package(
  INCLUDE_DIRS ${catkin_INCLUDE_DIRS} ${${PROJECT_NAME}_INCLUDE_DIRS}
  LIBRARIES ${PROJECT_NAME}
  CATKIN_DEPENDS ${${PROJECT_NAME}_DEPENDS}
)

include_directories( ${catkin_INCLUDE_DIRS} ${${PROJECT_NAME}_INCLUDE_DIRS} )

# Create library
add_library(template_lib src/template_library.cpp)
add_dependencies(template_lib ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
target_link_libraries(template_lib ${catkin_LIBRARIES})

add_library(template_ros_interface_lib src/template_ros_interface.cpp)
add_dependencies(template_ros_interface_lib ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
target_link_libraries(template_ros_interface_lib ${catkin_LIBRARIES} template_lib)

# Create executable (node)
add_executable(template_node src/template_node.cpp)
add_dependencies(template_node ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
target_link_libraries(template_node ${catkin_LIBRARIES} template_ros_interface_lib)


## Tests
#if (CATKIN_ENABLE_TESTING)
#  catkin_add_gtest(${PROJECT_NAME}_test src/tests/${PROJECT_NAME}_test.cpp)
#  target_link_libraries(${PROJECT_NAME}_test ${catkin_LIBRARIES})
#endif()

