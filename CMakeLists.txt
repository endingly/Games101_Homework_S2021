cmake_minimum_required(VERSION 3.20)
set(CMAKE_TOOLCHAIN_FILE "$ENV{VCPKG_ROOT}/scripts/buildsystems/vcpkg.cmake" CACHE STRING "Vcpkg toolchain file")
set(VCPKG_TARGET_TRIPLET "x64-windows" CACHE STRING "")
project(Games101_Homework)

# project settings
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

# package settings
find_package(Eigen3 CONFIG REQUIRED)
find_package(OpenCV CONFIG REQUIRED)
find_package(fmt CONFIG REQUIRED)
set(LIBRARY_REQUESTS Eigen3::Eigen ${OpenCV_LIBRARIES} fmt::fmt)

# source files and executable
file(GLOB_RECURSE HOMEWORK_ONE "homework_1/*.cpp" "homework_1/*.h")
add_executable(homework_1 ${HOMEWORK_ONE})
target_link_libraries(homework_1 PRIVATE ${LIBRARY_REQUESTS})

file(GLOB_RECURSE HOMEWORK_TWO "homework_2/*.cpp" "homework_2/*.h")
add_executable(homework_2 ${HOMEWORK_TWO})
target_link_libraries(homework_2 PRIVATE ${LIBRARY_REQUESTS})

file(GLOB_RECURSE HOMEWORK_THREE "homework_3/*.cpp" "homework_3/*.h")
add_executable(homework_3 ${HOMEWORK_THREE})
target_link_libraries(homework_3 PRIVATE ${LIBRARY_REQUESTS})
