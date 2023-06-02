file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_3 ${SOURCE_FILES})
target_link_libraries(homework_3 ${LIBRARY_REQUESTS})