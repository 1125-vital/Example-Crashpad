cmake_minimum_required(VERSION 3.10)
project(demo_linux LANGUAGES CXX)


add_executable(demo_linux demo.cpp)
target_include_directories(demo_linux PUBLIC ./include/crashpad ./include/crashpad/third_party/mini_chromium/mini_chromium)
target_link_directories(demo_linux PRIVATE
				./lib
    )
target_compile_features(demo_linux PRIVATE cxx_std_14)
target_link_libraries(demo_linux PRIVATE client pthread)
