cmake_minimum_required(VERSION 3.4)
project(formatter_ex)
set(CMAKE_CXX_STANDART 11)
set(CMAKE_CXX_STANDART_REQUIRED ON)
set(CMAKE_CURRENT_SOURCE_DIR ~/snoreoh/workspace/projects/lab4.1)
add_library(formatter_ex STATIC ${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex_lib/formatter_ex.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/formatter_lib)
target_link_libraries(formatter_ex formatter)



