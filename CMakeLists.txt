# CMake requirements
cmake_minimum_required(VERSION 3.0)
message(STATUS "Cmake version: ${CMAKE_VERSION}")

# Project Name
project(opencv_aruco)

# Compiler options
add_compile_options(-std=c++11)
add_compile_options(-Wall)
add_compile_options(-Wextra)

# OpenCV
find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

# Add code
add_executable(main src/main.cpp)
target_link_libraries(main ${OpenCV_LIBS})
