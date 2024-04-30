cmake_minimum_required(VERSION 3.11)

set(CMAKE_CXX_STANDARD 17)


project(faster_reader)

set(CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}/cmake_modules")

find_package(ROOT REQUIRED)

set(INCLUDES ${ROOT_INCLUDE_DIRS} )
include_directories(${INCLUDES})

add_executable(reader reader.cpp )
target_link_libraries( reader LINK_PUBLIC -lfasterac -lm ${ROOT_LIBRARIES} )

