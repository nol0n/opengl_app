cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(stb_image)

set(SOURCES
	sources/stb_image.c
)

set(HEADERS
	headers/stb_image.h
)

add_library(stb_image
	${SOURCES}
	${HEADERS}
)

target_include_directories(stb_image 
	PRIVATE headers
)
