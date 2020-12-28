cmake_minimum_required(VERSION 2.8.12)
project(myexe)

set(CMAKE_PREFIX_PATH ${CMAKE_CURRENT_SOURCE_DIR}/../out/)
find_package(mylib REQUIRED)

add_executable(myexe main.c)
target_link_libraries(myexe mylib)
install(TARGETS myexe DESTINATION bin)
