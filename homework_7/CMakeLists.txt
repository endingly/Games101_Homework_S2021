file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_7 ${SOURCE_FILES})
target_link_libraries(homework_7 ${LIBRARY_REQUESTS})