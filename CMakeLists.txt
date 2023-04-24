cmake_minimum_required(VERSION 2.6.0)

project(wx_something C CXX)

find_package(wxWidgets REQUIRED COMPONENTS net core base)
if (wxWidgets_USE_FILE)
    include(${wxWidgets_USE_FILE})
endif()

add_executable(${PROJECT_NAME} main.cpp simple.cpp simple.h)

target_link_libraries(${PROJECT_NAME} ${wxWidgets_LIBRARIES})
