cmake_minimum_required(VERSION 2.8)
project(red_triangle)

find_package(OpenGL REQUIRED)

add_subdirectory(glfw)

include_directories(glfw/include)
include_directories(glm)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -Wextra -std=c++11")

set(SOURCE_FILES main.cpp)
add_executable(red_triangle ${SOURCE_FILES})

target_link_libraries(red_triangle glfw ${GLFW_LIBRARIES} ${OPENGL_LIBRARY})
