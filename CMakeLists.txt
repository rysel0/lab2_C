cmake_minimum_required(VERSION 3.30.3 FATAL_ERROR)

project(Khayrulin_R)

set(CMAKE_WINDOWS_EXPORT_ALL_SYMBOLS ON) # возникали ошибки с чтением библиотеки

set(SOURCE_EXE main.cpp)	

include_directories(avg)

add_subdirectory(avg)

add_executable(Khayrulin ${SOURCE_EXE})

target_link_libraries(Khayrulin avg_stat
				avg_sh)

install(TARGETS Khayrulin
        CONFIGURATIONS Debug
        RUNTIME DESTINATION build/Debug/bin)