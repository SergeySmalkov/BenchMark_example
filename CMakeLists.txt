cmake_minimum_required(VERSION 3.23)
project(BenchMark_example)

set(CMAKE_CXX_STANDARD 20)

add_executable(BenchMark_example main.cpp)


add_executable(bench_exe ben.cpp)
add_subdirectory(lib/googletest)
add_subdirectory(lib/benchmark_lib)


target_link_libraries(bench_exe benchmark::benchmark)
target_link_libraries(bench_exe gtest gtest_main)


