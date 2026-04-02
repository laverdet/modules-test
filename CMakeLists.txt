cmake_minimum_required(VERSION 3.31 FATAL_ERROR)

# Project config
message(STATUS "Cmake version: ${CMAKE_VERSION}")
set(CMAKE_EXPERIMENTAL_CXX_IMPORT_STD "d0edc3af-4c50-42ea-a356-e2862fe7a444")

set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_STDLIB_MODULES_JSON "a.json")

project(isolated_vm LANGUAGES C CXX)
message(STATUS "Cmake C++ Standard Library: ${CMAKE_CXX_STANDARD_LIBRARY}")

# C++26 environment
set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_MODULE_STD ON)

add_executable(foo)
target_sources(foo PRIVATE a.cc)
