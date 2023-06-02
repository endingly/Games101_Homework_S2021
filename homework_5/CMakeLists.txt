file(GLOB_RECURSE SOURCE_FILES *.cpp *.hpp)
add_executable(homework_5 ${SOURCE_FILES})
target_link_libraries(homework_5 ${LIBRARY_REQUESTS})