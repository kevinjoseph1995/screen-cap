cmake_minimum_required(VERSION 3.20)
project(screen-cap)

find_program(CCACHE_FOUND ccache)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)
set(CMAKE_CXX_STANDARD 20)
if (CCACHE_FOUND)
    message(CCACHE_FOUND)
    set_property(GLOBAL PROPERTY RULE_LAUNCH_COMPILE ccache)
endif (CCACHE_FOUND)


add_subdirectory(src)

