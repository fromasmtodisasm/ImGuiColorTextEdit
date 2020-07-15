cmake_minimum_required(VERSION 3.16)

project(ImGuiColorTextEdit CXX)

add_library(${PROJECT_NAME}	STATIC 
	TextEditor.cpp 
	TextEditor.h
)
target_include_directories(${PROJECT_NAME} 
	PUBLIC
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
	$<INSTALL_INTERFACE:BlackBox/GuiTools/Editor>
)

find_package(imgui CONFIG REQUIRED)
target_link_libraries(${PROJECT_NAME} PUBLIC imgui::imgui)
