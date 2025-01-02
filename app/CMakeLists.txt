cmake_minimum_required(VERSION 3.15)
project(Downstream)

# specify the C++ standard
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)

find_package(MathFunctions 3.4.1 EXACT REQUIRED)
add_executable(myexe main.cpp)
message(STATUS "Include Dirs ${MathFunctions_INCLUDE_DIRS}")
include_directories(myexe MathFunctions_INCLUDE_DIRS )
target_link_libraries(myexe PRIVATE MathFunctions::MathFunctions)