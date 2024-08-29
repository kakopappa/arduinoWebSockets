# arduinoWebSockets

cmake_minimum_required(VERSION 3.15)

if(ESP_PLATFORM)
	# Build arduinoWebSockets as an ESP-IDF component
	idf_component_register(INCLUDE_DIRS src)
	return()
endif()

project(arduinoWebSockets VERSION 7.1.0)

if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
	include(CTest)
endif()

add_subdirectory(src)

# if(CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME AND BUILD_TESTING)
#	include(extras/CompileOptions.cmake)
#	add_subdirectory(extras/tests)
#	add_subdirectory(extras/fuzzing)
# endif()
