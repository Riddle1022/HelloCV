# 指定最低 CMake 版本
cmake_minimum_required(VERSION 3.10)
# 定义项目名
project(TextCrypto LANGUAGES CXX)

# 编译可执行程序，指定源文件
add_executable(TextCrypto main.cpp crypto.cpp)
# 指定头文件目录（让编译器找到 crypto.h）
target_include_directories(TextCrypto PUBLIC ./)
