cmake_minimum_required(VERSION 3.20.0)

# use packaged ninja builder
if(${CMAKE_HOST_SYSTEM_NAME} STREQUAL Windows)
set(CMAKE_MAKE_PROGRAM "${CMAKE_SOURCE_DIR}/extern/${CMAKE_HOST_SYSTEM_NAME}/ninja.exe" CACHE PATH "")
set(CMAKE_NINJA_PROGRAM "${CMAKE_SOURCE_DIR}/extern/${CMAKE_HOST_SYSTEM_NAME}/ninja.exe")
else()
set(CMAKE_MAKE_PROGRAM "${CMAKE_SOURCE_DIR}/extern/${CMAKE_HOST_SYSTEM_NAME}/ninja" CACHE PATH "")
set(CMAKE_NINJA_PROGRAM "${CMAKE_SOURCE_DIR}/extern/${CMAKE_HOST_SYSTEM_NAME}/ninja")
endif()
project(myfortran Fortran)

# once source file per line
set(EXAMPLE_SRC
    example.f90
)
add_executable(example ${EXAMPLE_SRC})

