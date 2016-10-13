cmake_minimum_required(VERSION 3.1)
project(sdfont)

find_package(Freetype)

add_executable(sdfont
	BinPacker.cpp
	BinPacker.hpp
	lodepng.cpp
	lodepng.h
	main.cpp
	stb_image.c
	stb_image.h
)

target_include_directories(sdfont PRIVATE ${FREETYPE_INCLUDE_DIRS})
target_link_libraries(sdfont ${FREETYPE_LIBRARIES})
