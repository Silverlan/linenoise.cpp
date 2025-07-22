cmake_minimum_required(VERSION 3.10)
project(linenoise CXX)

add_library(linenoise STATIC
    linenoise.cpp
)

target_include_directories(linenoise PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
)

install(TARGETS linenoise
    ARCHIVE DESTINATION lib
    PUBLIC_HEADER DESTINATION include
)
install(FILES linenoise.h DESTINATION include)
