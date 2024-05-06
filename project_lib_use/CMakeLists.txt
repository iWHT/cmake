# 这是一个cmake文件
cmake_minimum_required(VERSION 3.20)
project(app VERSION 1.0.0 LANGUAGES CXX DESCRIPTION "A simple program" HOMEPAGE_URL "www.a.com")

set(CMAKE_CXX_STANDARD 11)
set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR}/bin)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/include)
file(GLOB SRC_LIST ${CMAKE_CURRENT_SOURCE_DIR}/src/*.cpp)


#link_directories(${CMAKE_CURRENT_SOURCE_DIR}/lib1)
#link_directories(${CMAKE_CURRENT_SOURCE_DIR}/lib2)
#link_libraries(prog)

add_executable(app ${SRC_LIST})

target_link_directories(app PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/lib1)
target_link_libraries(app prog)


