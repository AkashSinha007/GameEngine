cmake_minimum_required(VERSION 3.22)

project(
    GameEngine 
    VERSION 1.0.0 
    LANGUAGES C CXX
)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)


set(CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake/")
include(AddGitSubmodule)
include(FetchContent)

FetchContent_Declare(
        spdlog
		GIT_REPOSITORY https://github.com/gabime/spdlog.git
		GIT_TAG v1.12.0
        GIT_SHALLOW TRUE
)
FetchContent_MakeAvailable(spdlog)


set(LIBRARY_NAME Hazel)
set(EXECUTABLE_NAME Sandbox)

add_subdirectory(Hazel)
add_subdirectory(Sandbox)