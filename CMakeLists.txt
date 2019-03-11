cmake_minimum_required(VERSION 3.4)
project(Sophus VERSION 1.0.0)

find_package(catkin_simple REQUIRED)
catkin_simple(ALL_DEPS_REQUIRED)

#############
# LIBRARIES #
#############
add_definitions(-std=c++11)

#############
# QTCREATOR #
#############
FILE(GLOB_RECURSE LibFiles "include/*hpp")
add_custom_target(headers SOURCES ${LibFiles})
  
##########
# EXPORT #
##########
cs_install()
cs_export()

