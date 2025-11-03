cmake_minimum_required(VERSION 3.10)

project(Lab2QRCode)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_AUTOMOC ON)

set(EXECUTABLE_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/build/${CMAKE_BUILD_TYPE}/bin)

include_directories(include)
find_package(Qt5 REQUIRED COMPONENTS Core Widgets)
file(GLOB SOURCES "src/*.cpp")

add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} 
    Qt5::Core
    Qt5::Widgets
)