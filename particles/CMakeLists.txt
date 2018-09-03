project(Particles)

set(EXECUTABLE_NAME ${PROJECT_NAME})

file(GLOB SOURCES src/*.cpp)

add_executable(${EXECUTABLE_NAME} ${SOURCES})

if(NOT ${CMAKE_BUILD_TYPE} STREQUAL "Release")
    MESSAGE("Debug mode")
    add_definitions ("-Wall -std=c++11 -g3")
else()
    MESSAGE("Release mode")
    add_definitions ("-Wall -std=c++11 -g3")
endif()

include_directories(inc)

target_link_libraries(${EXECUTABLE_NAME} ${OPENGL_LIBRARIES} glfw ${GLFW_LIBRARIES})
