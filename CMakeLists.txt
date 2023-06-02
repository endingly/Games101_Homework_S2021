cmake_minimum_required(VERSION 3.20)
project(Games101_Homework)

# project settings
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)
add_compile_options(/utf-8)

###################################### package settings#########################################
# vcpkg package settings
find_package(Eigen3 CONFIG REQUIRED)
find_package(OpenCV CONFIG REQUIRED)
find_package(fmt CONFIG REQUIRED)
set(LIBRARY_REQUESTS Eigen3::Eigen ${OpenCV_LIBRARIES} fmt::fmt)
################################################################################################

# target list
add_subdirectory(homework_1)
add_subdirectory(homework_2)
add_subdirectory(homework_3)
add_subdirectory(homework_4)
add_subdirectory(homework_5)
add_subdirectory(homework_6)
add_subdirectory(homework_7)
add_subdirectory(homework_8)