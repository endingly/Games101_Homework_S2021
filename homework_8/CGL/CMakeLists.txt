find_package(glfw3 CONFIG REQUIRED)
find_package(GLEW REQUIRED)
find_package(Freetype REQUIRED)
# find_package(OpenGL REQUIRED)

# target CGL
file(GLOB_RECURSE CGL_SOURCES_FILES src/*.cpp)
add_library(CGL STATIC ${CGL_SOURCES_FILES})
target_link_libraries(CGL PUBLIC glfw GLEW::GLEW Freetype::Freetype)# OpenGL::GL)
target_include_directories(CGL PUBLIC include)