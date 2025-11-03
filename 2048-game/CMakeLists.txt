cmake_minimum_required(VERSION 3.15)
project(2048Game)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# For macOS with Homebrew
set(CMAKE_PREFIX_PATH "/opt/homebrew" ${CMAKE_PREFIX_PATH})

# Find SFML 3
find_package(SFML 3.0 COMPONENTS Graphics Window System REQUIRED)

# Include directories
include_directories(include)

# Source files
set(SOURCES
    src/main.cpp
    # src/Game.cpp
    # src/Board.cpp
    # src/Renderer.cpp
)

# Create executable
add_executable(2048Game ${SOURCES})

# Link SFML (note the different syntax for SFML 3)
target_link_libraries(2048Game SFML::Graphics SFML::Window SFML::System)