cmake_minimum_required(VERSION 3.9)
project(MyPWHelloWorld CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
message(STATUS "Using C++${CMAKE_CXX_STANDARD}")

add_library(main main.cpp)
add_library(hello_fn hello_fn.cpp)

add_executable(exe main hello_fn)
#target_link_libraries(main hello_fn)

include(CTest)
add_test (MainTest exe )
