add_subdirectory(CGL)

if(WIN32)
    find_package(unofficial-getopt-win32 REQUIRED)
endif()

# target homework_8
file(GLOB_RECURSE SOURCE_FILES *.cpp)
add_executable(homework_8 ${SOURCE_FILES})
target_link_libraries(homework_8 PRIVATE CGL unofficial::getopt-win32::getopt)

# target_include_directories(homework_8 PRIVATE ./CGL/include)