add_subdirectory(CGL)

# target homework_8
file(GLOB_RECURSE SOURCE_FILES *.cpp)
add_executable(homework_8 ${SOURCE_FILES})

if(WIN32)
    find_package(unofficial-getopt-win32 REQUIRED)
    target_link_libraries(homework_8 PRIVATE CGL unofficial::getopt-win32::getopt)
else()
    target_link_libraries(homework_8 PRIVATE CGL)
endif()