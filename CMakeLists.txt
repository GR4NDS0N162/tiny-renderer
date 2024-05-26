cmake_minimum_required(VERSION 3.28.1)

project(tiny-renderer)

set(SOURCE_EXE main.cpp)

set(SOURCE_LIB tgaimage.cpp)

add_library(tgaimage STATIC ${SOURCE_LIB})

add_executable(main ${SOURCE_EXE})

target_link_libraries(main tgaimage)
