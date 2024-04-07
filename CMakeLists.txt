cmake_minimum_required(VERSION 3.0)
project(YourProjectName)

# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# 添加可执行文件并包含源文件
add_executable(YourExecutable example.cpp ThreadPool.h)
# 找到并链接需要的线程库
find_package(Threads REQUIRED)
target_link_libraries(YourExecutable Threads::Threads)

