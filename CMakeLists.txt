cmake_minimum_required(VERSION 3.7)

set(PNAME spaceGame)
set(CMAKE_CXX_STANDARD 14)
set(SFML_VERSION 2.3)

project(${PNAME})

set(SFML_COMPONENTS graphics window system)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
find_package(SFML ${SFML_VERSION} COMPONENTS ${SFML_COMPONENTS} REQUIRED)

include_directories(${SFML_INCLUDE_DIR})

set(SOURCE_FILES main.cpp)
add_executable(spaceGame ${SOURCE_FILES})
target_link_libraries(${PNAME} ${SFML_LIBRARIES} ${SFML_DEPENDENCIES})