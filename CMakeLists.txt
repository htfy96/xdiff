cmake_minimum_required(VERSION 3.11)

project(xdiff VERSION "0.1" LANGUAGES C)

file(GLOB SRC "*.c" "*.h")
list(SORT SRC)

add_library(xdiff OBJECT ${SRC})

target_include_directories(xdiff PUBLIC ${CMAKE_PROJECT_DIR})
