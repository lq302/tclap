cmake_minimum_required(VERSION 3.0.0 FATAL_ERROR)
project(tclap)

add_library(tclap INTERFACE)
target_include_directories(tclap INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}/include")
