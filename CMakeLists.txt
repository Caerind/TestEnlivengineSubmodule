cmake_minimum_required(VERSION 3.12...3.15)

project(MyGameProject
    VERSION 0.3
    DESCRIPTION "MyGame"
    LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED TRUE)
set(CMAKE_CXX_EXTENSIONS OFF)

if (CMAKE_PROJECT_NAME STREQUAL PROJECT_NAME)
	enable_testing()
endif()

# Used to have a good display look in IDE
set_property(GLOBAL PROPERTY USE_FOLDERS ON)
set_property(GLOBAL PROPERTY PREDEFINED_TARGETS_FOLDER "CMake")

add_subdirectory(Enlivengine)
add_subdirectory(MyGame)

set_property(DIRECTORY PROPERTY VS_STARTUP_PROJECT MyGame)