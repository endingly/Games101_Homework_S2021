file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_4 ${SOURCE_FILES})
target_link_libraries(homework_4 ${LIBRARY_REQUESTS})