add_library(${LIBRARY_NAME} SHARED
            #Log
            Hazel/Log.h
            Hazel/Log.cpp 

            #Application
            Hazel/Application.cpp 
            Hazel/Application.h
            Hazel/EntryPoint.h

            # Events
            Hazel/Events/Event.h
            Hazel/Events/MouseEvent.h
            Hazel/Events/KeyEvent.h
            Hazel/Events/ApplicationEvent.h
            )

target_link_libraries(${LIBRARY_NAME} PUBLIC 
                        spdlog::spdlog
                    )
target_include_directories(${LIBRARY_NAME} PUBLIC "./")