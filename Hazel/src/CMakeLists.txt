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

            #pre-compiled header
            hzpch.h
            hzpch.cpp

            #Windows and Platform
            Hazel/Window.h 
            Platform/Mac/MacWindow.h
            Platform/Mac/MacWindow.cpp
            )

target_link_libraries(${LIBRARY_NAME} PUBLIC 
                        spdlog::spdlog
                        glfw
                        glad
                        ${OPENGL_LIBRARY} # filled by "find_package(OpenGL REQUIRED)"
                    )
target_include_directories(${LIBRARY_NAME} PUBLIC "./" 
                            ${glfw_SOURCE_DIR}/include/)