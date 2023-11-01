cmake_minimum_required(VERSION 3.3)
project(find-pan)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

set(SOURCE_FILES
    find-pan.c)

add_executable(find-pan ${SOURCE_FILES})

install(PROGRAMS find-pan DESTINATION /usr/local/bin)
