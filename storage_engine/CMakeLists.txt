cmake_minimum_required(VERSION 4.1)

project(nas)

add_library(storage_engine_lib
        src/utils/Logger.h
        src/utils/Logger.cpp
        src/core/Engine.cpp
        src/core/Engine.h
)

add_executable(storage_engine
        src/main.cpp
)

target_link_libraries(storage_engine PRIVATE storage_engine_lib)
