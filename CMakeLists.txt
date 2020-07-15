cmake_minimum_required(VERSION 3.16)

project(ImGuiColorTextEdit CXX)

add_library(${PROJECT_NAME} STATIC TextEditor.cpp)

target_include_directories(${PROJECT_NAME} 
	PUBLIC
	$<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
	$<INSTALL_INTERFACE:BlackBox/GuiTools/Editor>
)
