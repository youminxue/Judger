cmake_minimum_required(VERSION 2.5)
project(container C)

#set(CMAKE_VERBOSE_MAKEFILE ON)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}/output)

set(CMAKE_C_FLAGS "-g -Wall -Werror -O2 -std=c99 -pie -fPIC")

file(GLOB SOURCE "src/*.c" "src/rules/*.c")
add_executable(container ${SOURCE})
target_link_libraries(container pthread seccomp)