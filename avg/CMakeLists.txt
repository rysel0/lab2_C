cmake_minimum_required(VERSION 3.30.3 FATAL_ERROR)

project(AvgFunc)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON)

set(SOURCE_LIB avgf.cpp)

add_library(avg_stat STATIC ${SOURCE_LIB})

add_library(avg_sh SHARED ${SOURCE_LIB})
