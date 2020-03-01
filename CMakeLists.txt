cmake_minimum_required(VERSION 3.13)
project(LearnOpenGL)

set(CMAKE_CXX_STANDARD 14)

#find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)

add_library(glad STATIC glad.c)
add_executable(LearnOpenGL main.cpp)
add_executable(window
        01-window.c)

#set(CMAKE_C_FLAGS "${CMAKE_CXX_FLAGS} -framework Cocoa -framework OpenGL -framework IOKit")

include_directories(/usr/local/include)
link_directories(/usr/local/lib)
target_link_libraries(window
        glfw
        glad
        )