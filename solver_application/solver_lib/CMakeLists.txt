cmake_minimum_required(VERSION 2.8) 
project(solver_lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
add_library(solver_lib STATIC ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)


