cmake_minimum_required(VERSION 2.8 FATAL_ERROR)
set (CMAKE_CXX_STANDARD 11)

project(clusterize)

find_package(PCL 1.2 REQUIRED)

include_directories(${PCL_INCLUDE_DIRS})
link_directories(${PCL_LIBRARY_DIRS})
add_definitions(${PCL_DEFINITIONS})

add_executable (clusterize clusterize.cc)
target_link_libraries (clusterize ${PCL_LIBRARIES})