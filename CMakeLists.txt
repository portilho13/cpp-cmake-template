cmake_minimum_required(VERSION 3.10) # Minimum required version of CMake

project(project_name) # Project name

# Set the C++ standard to the most recent one supported by your compiler
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the include directory
include_directories(include lib)

# Find all .cpp files in the source and lib directories
file(GLOB SOURCE_FILES "src/*.cpp")
file(GLOB LIB_FILES "lib/*.cpp")

# Combine all source files
set(ALL_SOURCES ${SOURCE_FILES} ${LIB_FILES})

# Print a message with the sources for debugging purposes
message("SOURCES: ${ALL_SOURCES}")

# Define the executable and its source files
add_executable(project_name ${ALL_SOURCES})