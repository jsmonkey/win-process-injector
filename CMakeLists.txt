cmake_minimum_required(VERSION 3.0)

project(win_process_injector)

set(CMAKE_CXX_FLAGS_RELEASE "/MT")

set(LIB_SRC
    src/process_manager.cc)

set(LIB_H
    src/process_manager.h)

add_library(win_process_injector_lib STATIC ${LIB_SRC})

install(TARGETS win_process_injector_lib DESTINATION ${PROJECT_SOURCE_DIR}/bin)
install(FILES ${LIB_H} DESTINATION ${PROJECT_SOURCE_DIR}/include)