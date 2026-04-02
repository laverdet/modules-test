cmake_minimum_required(VERSION 4.3.0 FATAL_ERROR)
message(STATUS "Cmake version: ${CMAKE_VERSION}")

# Project config
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD 26)
set(CMAKE_CXX_STDLIB_MODULES_JSON ms-stl.modules.json)
set(CMAKE_EXPERIMENTAL_CXX_IMPORT_STD "451f2fe2-a8a2-47c3-bc32-94786d8fc91b")
project(isolated_vm LANGUAGES C CXX)
message(STATUS "Cmake C++ Standard Library: ${CMAKE_CXX_STANDARD_LIBRARY}")

# C++26 environment
set(CMAKE_CXX_MODULE_STD ON)

add_executable(foo)
target_sources(foo PRIVATE a.cc)
