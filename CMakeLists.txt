cmake_minimum_required(VERSION 3.14)
project(ImGuizmo)

file(GLOB IMGUIZMO_SRC
    "ImGuizmo.cpp"
    "ImGuizmo.h"
)

add_library(ImGuizmo STATIC ${IMGUIZMO_SRC})

target_include_directories(ImGuizmo PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})
target_link_libraries(ImGuizmo PUBLIC imgui)

# Define IMGUI_DEFINE_MATH_OPERATORS
target_compile_definitions(ImGuizmo PUBLIC IMGUI_DEFINE_MATH_OPERATORS)

