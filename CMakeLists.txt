cmake_minimum_required(VERSION 3.10.0)

project(LearnOpenGL VERSION 0.1.0 LANGUAGES C CXX)

# 包含glad头文件
include_directories(./glad/include)

# 包含glfw头文件，可能版本不用路径会有所差异
include_directories(/opt/homebrew/Cellar/glfw/3.4/include)
# 链接glfw库，可能版本不用路径会有所差异
link_directories(/opt/homebrew/Cellar/glfw/3.4/lib)


# 设置可执行文件输出路径
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_SOURCE_DIR}/bin)

add_executable(LearnOpenGL ./glad/src/glad.c main.cpp)
# 目标链接库
target_link_libraries(
    LearnOpenGL # demo_cpp是项目名称
    glfw
)