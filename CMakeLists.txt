cmake_minimum_required(VERSION 3.21)
project(imguizmo)

add_library(imguizmo STATIC "ImGuizmo.h" "ImGuizmo.cpp")
target_include_directories(imguizmo PRIVATE ../imgui)
