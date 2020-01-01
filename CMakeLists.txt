﻿cmake_minimum_required(VERSION 3.0)

project(recurse-builder)

add_subdirectory(dependencies/glad)
include_directories(dependencies/glad/include)
add_subdirectory(dependencies/glfw)
include_directories(dependencies/glfw/include)
add_subdirectory(dependencies/glm)
include_directories(dependencies/glm)

add_executable(recurse-builder src/main.cc)
target_link_libraries(recurse-builder glad)
target_link_libraries(recurse-builder glfw ${GLFW_LIBRARIES})