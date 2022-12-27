cmake_minimum_required (VERSION 3.5)
project (Memory-Allocator-Examples LANGUAGES CXX)

set(SOURCES src/AllocatorI.cpp
   	src/CAllocator.cpp
   	src/LinearAllocator.cpp
   	src/StackAllocator
   	src/Benchmark.cpp 
	src/main.cpp)

add_executable(main ${SOURCES})
target_include_directories(main PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/includes)
target_compile_features(main PRIVATE cxx_std_11)