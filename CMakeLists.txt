cmake_minimum_required(VERSION 3.0)
project(QProgressIndicator)

find_package(Qt5 REQUIRED COMPONENTS Core Widgets)

add_library(QProgressIndicator "${CMAKE_CURRENT_SOURCE_DIR}/QProgressIndicator.cpp")

set_property(TARGET QProgressIndicator APPEND
             PROPERTY INTERFACE_INCLUDE_DIRECTORIES "${CMAKE_CURRENT_SOURCE_DIR}")

target_link_libraries(QProgressIndicator Qt5::Core Qt5::Widgets)
