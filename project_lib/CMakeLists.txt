# 这是一个cmake文件
cmake_minimum_required(VERSION 3.0)
project(prog VERSION 1.0.0 LANGUAGES CXX DESCRIPTION "A simple program" HOMEPAGE_URL "www.a.com")

set(CMAKE_CXX_STANDARD 11)
set(LIBRARY_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/lib)

message(STATUS "This is SOURCE dir " ${PROJECT_SOURCE_DIR})
message(STATUS "This is BUILD dir " ${PROJECT_BINARY_DIR})
message(STATUS "This is LIBRARY_OUTPUT_PATH " ${LIBRARY_OUTPUT_PATH})

message(STATUS "This is CMAKE_CURRENT_SOURCE_DIR " ${CMAKE_CURRENT_SOURCE_DIR})
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
file(GLOB SRC_LIST ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)

add_library(prog SHARED ${SRC_LIST})
#add_library(prog STATIC ${SRC_LIST})
