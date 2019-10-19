#setting the project variables
set(TARGET_APPLICATION_NAME "executable")
set(HEADERS_DIRECTORY "include")
set(SOURCES_DIRECTORY "src")
set(CMAKE_CXX_STANDARD 14)
###########################################

project(executable_cmake_proj)
cmake_minimum_required(VERSION 3.0.0)

#setting the soures and headers directory
file(GLOB_RECURSE SOURCES "${SOURCES_DIRECTORY}/*.cpp")

include_directories(${HEADERS_DIRECTORY})

#adding headers makes to make dependencies in makefile right
add_executable(${TARGET_APPLICATION_NAME} ${SOURCES})
