cmake_minimum_required(VERSION 3.0)
set(APP_NAME "gtool")
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/dist")
set(CMAKE_C_COMPILER "c:/mingw64/bin/gcc.exe")
set(CMAKE_CXX_COMPILER "c:/mingw64/bin/g++.exe")

file(GLOB_RECURSE SOURCES "src/*.cpp" CONFIGURE_DEPEND)
file(GLOB_RECURSE HEADERS "src/*.h" CONFIGURE_DEPEND)

project(${APP_NAME})
#add_subdirectory(modules/cli11)
add_executable(${APP_NAME} src/main.cpp ${SOURCES} ${HEADERS})
