cmake_minimum_required(VERSION 3.0)

project(nt_app VERSION 1.0)

add_subdirectory(../nt-io nt-io)
add_subdirectory(../nt-vision nt-vision)

add_executable(nt_app src/main.cpp)

target_compile_features(nt_app PRIVATE cxx_std_14)

target_include_directories(nt_app PRIVATE include/)
target_link_libraries(nt_app PRIVATE nt_vision nt_io)
