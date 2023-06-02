file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_2 ${SOURCE_FILES})
target_link_libraries(homework_2 ${LIBRARY_REQUESTS})