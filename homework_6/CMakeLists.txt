file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_6 ${SOURCE_FILES})
target_link_libraries(homework_6 ${LIBRARY_REQUESTS})