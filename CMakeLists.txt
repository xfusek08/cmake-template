cmake_minimum_required(VERSION 3.22.1)

# Project HelloWorld
# ------------------

# Find all source files in src directory: https://stackoverflow.com/a/47428496
# IMPORTANT NOTES:
#  * When using Visual Studio avoid this method and let Visual Studio manage the list source files int this file
#  * Otherwise, manual reconfiguration of project is needed when adding/removing files
file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*.cpp" "src/*.h")

project(HelloWorld VERSION 1.0)
add_executable(HelloWorld ${SOURCES})
target_include_directories(HelloWorld PUBLIC src/)
