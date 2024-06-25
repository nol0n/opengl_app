cmake_minimum_required(VERSION 3.12 FATAL_ERROR)

add_executable(app 
	main.cpp
)

add_subdirectory(lib_example)

add_subdirectory(shader_class)

target_include_directories(app
  	PRIVATE lib_example/headers
  	PRIVATE shader_class/headers
  	PRIVATE ../dependencies/glad/include
  	PRIVATE ../dependencies/stb_image/headers
)

target_link_libraries(app
	PRIVATE glfw
	PRIVATE glad
	PRIVATE glm
	PRIVATE stb_image
	PRIVATE lib_example
	PRIVATE shader_class
)
