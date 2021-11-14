cmake_minimum_required(VERSION 3.10)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# set the project name
project(HelloWindow)
# add the executable
add_executable(HelloWindow main.cpp glad.c)

target_include_directories(HelloWindow PRIVATE glad/include)

find_package(glfw3 3.3 REQUIRED)
target_link_libraries(HelloWindow glfw)

find_package(OpenGL REQUIRED)
target_link_libraries(HelloWindow OpenGL::GL ${CMAKE_DL_LIBS})


