cmake_minimum_required(VERSION 2.8.3)
project(human_model)

find_package(catkin REQUIRED COMPONENTS
			 roscpp
			 tf)

catkin_package()

include_directories(${catkin_INCLUDE_DIRS})

# Install generated urdf files
install(DIRECTORY urdf/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/urdf)
# Install collada files
install(DIRECTORY meshes/
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/meshes)
