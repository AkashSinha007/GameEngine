add_library(${LIBRARY_NAME} SHARED Hazel/Application.cpp Hazel/Application.h)
target_include_directories(${LIBRARY_NAME} PUBLIC "./")