cmake_minimum_required(VERSION 3.20)
project(learn-opengl CXX)

set(CMAKE_CXX_STANDARD 11)

find_package(PkgConfig)
pkg_check_modules(GLFW glfw3 gl epoxy)

include_directories(${GLFW_INCLUDE_DIRS})

add_executable(learn-opengl main.cpp)
target_link_libraries(learn-opengl ${GLFW_LINK_LIBRARIES})