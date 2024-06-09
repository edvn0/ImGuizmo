cmake_minimum_required(VERSION 3.2)
project(imguizmo)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} -DVK_PROTOTYPES")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DVK_PROTOTYPES")

set(LIBRARY_NAME imguizmo)

file(GLOB sources *.cpp)

add_library(${LIBRARY_NAME} STATIC ${sources})
target_include_directories(
   ${LIBRARY_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR} ../imgui
   $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>)
