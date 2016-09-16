cmake_minimum_required(VERSION 3.0)
project(FDtest)

find_package(OpenCV REQUIRED)

include_directories(./include/)
include_directories(./include/classfier/)
include_directories(./include/feat)
include_directories(./include/io)
include_directories(./include/util)

file(GLOB HEADERS include/*/*.h* include/*.h*)
file(GLOB SOURCES *.c*)

set(ALL_FILES ${HEADERS} ${SOURCES})

add_executable(${PROJECT_NAME} ${ALL_FILES})
target_link_libraries(${PROJECT_NAME} ${FD.lib} ${OpenCV_LIBS})