cmake_minimum_required(VERSION 2.8.0)

project(ComputeShaders)

find_package(OpenGL REQUIRED)

include_directories(${OPENGL_INCLUDE_DIR})
include_directories(glfw-master/include)

add_subdirectory(glfw-master)
add_subdirectory(particles)