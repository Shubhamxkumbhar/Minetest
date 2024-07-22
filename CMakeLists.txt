cmake_minimum_required(VERSION 3.10)

# Set the project name
project(Minetest)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the executable
add_executable(Minetest 
    src/main.cpp 
    src/client/client.cpp
    src/server/server.cpp
    src/game/game.cpp
    src/utilities/util.cpp
    # Add other source files here
)

# Include directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# Link libraries (if any)
# target_link_libraries(Minetest PRIVATE some_library)
