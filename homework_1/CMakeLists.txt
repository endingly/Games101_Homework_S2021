file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_1 ${SOURCE_FILES})
target_link_libraries(homework_1 ${LIBRARY_REQUESTS})