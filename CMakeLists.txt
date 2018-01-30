cmake_minimum_required(VERSION 3.0)

project(win_process_injector)

set(LIB_SRC
    src/process_manager.cc)

add_library(win_process_injector STATIC ${LIB_SRC})

target_include_directories(win_process_injector PUBLIC ${PROJECT_SOURCE_DIR}/include)