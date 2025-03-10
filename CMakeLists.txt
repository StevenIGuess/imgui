cmake_minimum_required(VERSION 3.18)

project(ImGui)

set(CMAKE_CXX_STANDART 14)

set(IMGUI_SOURCES
    imgui.cpp
    imgui_demo.cpp
    imgui_tables.cpp
    imgui_draw.cpp
    imgui_widgets.cpp
    backends/imgui_impl_glfw.cpp
    backends/imgui_impl_vulkan.cpp
    backends/imgui_impl_opengl3.cpp
    #backends/imgui_impl_glut.cpp
    #uncomment this for glut support
)

add_library(imgui STATIC ${IMGUI_SOURCES})

target_include_directories(imgui PUBLIC ${CMAKE_CURRENT_SOURCE_DIR})


