cmake_minimum_required(VERSION 3.31 FATAL_ERROR)

# Project config
message(STATUS "Cmake version: ${CMAKE_VERSION}")
if (CMAKE_VERSION VERSION_GREATER_EQUAL "4.3.0")
  set(CMAKE_EXPERIMENTAL_CXX_IMPORT_STD "451f2fe2-a8a2-47c3-bc32-94786d8fc91b")
else()
  set(CMAKE_EXPERIMENTAL_CXX_IMPORT_STD "d0edc3af-4c50-42ea-a356-e2862fe7a444")
endif()
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD 26)
project(isolated_vm LANGUAGES C CXX)
message(STATUS "Cmake C++ Standard Library: ${CMAKE_CXX_STANDARD_LIBRARY}")

# C++26 environment
set(CMAKE_CXX_MODULE_STD ON)

add_executable(foo)
target_sources(foo PRIVATE a.cc)
