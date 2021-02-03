cmake_minimum_required(VERSION 3.13)
project(glad C)

add_library(glad STATIC)
target_sources(glad
    PRIVATE
   "${CMAKE_CURRENT_SOURCE_DIR}/src/glad.c"
   "${CMAKE_CURRENT_SOURCE_DIR}/include/glad/glad.h"
   "${CMAKE_CURRENT_SOURCE_DIR}/include/KHR/khrplatform.h"
)
target_include_directories(glad PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/include")
