# Describing what CMake version we need
# Change this if you happen to be working with different version
# of CMake
cmake_minimum_required(VERSION 2.8)

# Projects name
project(how_to_cmake)

# Adding a library
add_library(
    hello #we can specify what type of library here: STATIC SHARED or MODULAR
	hello.h
	hello.c
    )

# Creates an executable by compiling and linking a list of space 
# separated C files.
add_executable(program_one hello_world.c)

# Linking libraries to executable
target_link_libraries(program_one PRIVATE hello)
