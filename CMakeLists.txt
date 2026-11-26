cmake_minimum_required(VERSION 3.20)
project(MyGLApp LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(OpenGL REQUIRED)
find_package(glfw3 REQUIRED)
find_package(GLEW REQUIRED)
find_package(glm REQUIRED)

add_executable(app src/main.cpp)

target_link_libraries(app PRIVATE
    OpenGL::GL
    glfw
    GLEW::GLEW
    glm::glm
)