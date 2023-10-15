cmake_minimum_required(VERSION 3.15)

project(n3dsdisasm C)

add_subdirectory(capstone)

set(SOURCES main.c disasm.c)
add_executable(n3dsdisasm ${SOURCES})
target_link_libraries(n3dsdisasm capstone::capstone)
