cmake_minimum_required(VERSION 3.22)

project(
    GameEngine 
    VERSION 1.0.0 
    LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

set(LIBRARY_NAME Hazel)
set(EXECUTABLE_NAME Sandbox)

add_subdirectory(Hazel)
add_subdirectory(Sandbox)