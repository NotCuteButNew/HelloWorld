cmake_minimum_required(VERSION 3.0.0)
project(lesson01 VERSION 0.1.0 LANGUAGES C CXX)

include(CTest)
enable_testing()

add_library(hello SHARED hello.h hello.cpp)
add_executable(main main.cpp)

target_link_libraries(main hello)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED)
set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
include(CPack)
