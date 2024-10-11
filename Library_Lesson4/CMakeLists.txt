cmake_minimum_required(VERSION 3.10)

project(MatchstickGameLib)

set(CMAKE_CXX_STANDARD 11)

add_library(MatchstickGameLib STATIC src/Game.cpp src/Player.cpp)

target_include_directories(MatchstickGameLib PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

add_executable(MatchstickGame src/Library_Lesson4.cpp)

target_link_libraries(MatchstickGame PRIVATE MatchstickGameLib)
