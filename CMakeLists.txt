cmake_minimum_required(VERSION 3.10)

# Set the project name and version
project(MyProject VERSION 1.0)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the include directory
include_directories(${PROJECT_SOURCE_DIR}/include)

# Add the source files (adjust the path as necessary)
file(GLOB SOURCES "${PROJECT_SOURCE_DIR}/*.cpp")

# Check if any source files were found
if(NOT SOURCES)
    message(FATAL_ERROR "No source files found. Check the specified directory and file extensions.")
endif()

# Add the executable
add_executable(MyProject ${SOURCES})

# Link libraries if necessary
# target_link_libraries(MyProject PRIVATE SomeLibrary)
