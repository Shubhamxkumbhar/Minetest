cmake_minimum_required(VERSION 3.10)

# Set the project name
project(Minetest)

# Specify the C++ standard
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Add the executable
add_executable(Minetest
    # Add the source files here
    src/main.cpp 
    # Include other source files as needed
)

# Include directories
include_directories(${CMAKE_SOURCE_DIR}/include)

# Link libraries (if any)
# target_link_libraries(Minetest PRIVATE some_library)

# Add subdirectories for additional modules or parts of the project
add_subdirectory(client)
add_subdirectory(clientmods)
add_subdirectory(doc)
add_subdirectory(fonts)
add_subdirectory(games)
add_subdirectory(locale)
add_subdirectory(mods)
add_subdirectory(textures)
add_subdirectory(worlds)

# Optional: add definitions if necessary
# add_definitions(-DSOME_DEFINITION)
