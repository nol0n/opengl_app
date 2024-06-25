cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(lib_example)

set(SOURCES
    sources/lib_example.cpp
)

set(HEADERS
    headers/lib_example.hpp
)

add_library(lib_example
    ${SOURCES}
    ${HEADERS}
)

target_include_directories(lib_example
    PRIVATE headers
)
