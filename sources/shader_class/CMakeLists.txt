cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

project(shader_class)

set(SOURCES	
	sources/shader_class.cpp
)

set(HEADERS
	headers/shader_class.hpp
)

add_library(shader_class
	${SOURCES}
	${HEADERS}
)

target_include_directories(shader_class
	PRIVATE headers
	PRIVATE ../../dependencies/glad/include
)

target_link_libraries(shader_class
	PRIVATE glad
)
