add_library(${LIBRARY_NAME} SHARED
            Hazel/Log.h
            Hazel/Log.cpp 
            Hazel/Application.cpp 
            Hazel/Application.h
            Hazel/EntryPoint.h
            )

target_link_libraries(${LIBRARY_NAME} PRIVATE 
                        spdlog::spdlog
                    )
target_include_directories(${LIBRARY_NAME} PUBLIC "./")