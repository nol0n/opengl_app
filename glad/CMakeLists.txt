cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(glad)

set(SOURCES
	src/gl.c
)

add_library(glad 
	${SOURCES}
)

target_include_directories(glad 
	PRIVATE include/
)
