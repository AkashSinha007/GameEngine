add_executable(${EXECUTABLE_NAME} SandboxApp.cpp)

target_include_directories(Hazel PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

target_link_libraries(${EXECUTABLE_NAME} PRIVATE 
                        ${LIBRARY_NAME}
                        )
