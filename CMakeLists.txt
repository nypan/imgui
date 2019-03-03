cmake_minimum_required(VERSION 3.12)

# version is fake
project(imgui VERSION 1.0.0)

set (SRCS 
imconfig.h
imgui.h
imgui.cpp
imgui_draw.cpp
imgui_internal.h
imgui_widgets.cpp
imstb_rectpack.h
imstb_textedit.h
imstb_truetype.h
imgui_demo.cpp
)

add_library(
    imgui STATIC 
    ${SRCS}
)

set_property(TARGET imgui PROPERTY CXX_STANDARD 17)    

TARGET_LINK_LIBRARIES(
	imgui PRIVATE 
)

target_include_directories(imgui PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}"  )
#target_compile_definitions(azzar PRIVATE )