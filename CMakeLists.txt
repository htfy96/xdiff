cmake_minimum_required(VERSION 3.11)

project(xdiff VERSION "0.1" LANGUAGES C)

file(GLOB SRC "*.c" "*.h")
list(SORT SRC)

add_library(xdifflib ${SRC})
set_target_properties(xdifflib PROPERTIES CXX_EXTENSIONS OFF)

add_library(xdiff INTERFACE)
target_link_libraries(xdiff INTERFACE xdifflib)
target_include_directories(xdiff INTERFACE ${PROJECT_SOURCE_DIR})
