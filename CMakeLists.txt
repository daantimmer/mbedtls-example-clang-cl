cmake_minimum_required(VERSION 3.24)

project(example LANGUAGES C CXX VERSION 1.0.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED On)

if (CMAKE_SYSTEM_NAME STREQUAL "Windows")
    add_compile_options($<$<CXX_COMPILER_ID:MSVC>:/EHsc>)
endif()

include(FetchContent)

add_subdirectory(external)

add_executable(example main.cpp)
target_link_libraries(example mbedtls)
