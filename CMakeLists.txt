# CMakeLists.txt
cmake_minimum_required(VERSION 3.10)
project(OpenGLProject LANGUAGES CXX)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Specify source files
set(SOURCES
    src/main.cpp
)

# Add an executable target
add_executable(my_opengl_app ${SOURCES})

# Find GLFW
find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(my_opengl_app PRIVATE glfw)

# Find GLEW
find_package(GLEW REQUIRED)
target_link_libraries(my_opengl_app PRIVATE GLEW::GLEW)

# Find OpenGL
find_package(OpenGL REQUIRED)
target_link_libraries(my_opengl_app PRIVATE OpenGL::GL)

# Include directories for GLM (header-only, no explicit linking needed)
# Depending on your GLM installation, you might need to specify the include directory.
# Often, CMake's find_package for GLM isn't available, so you might add it like this:
# For Arch Linux, GLM headers are typically in /usr/include/glm, which is usually found by default.
# If not, you might need:
# include_directories(/usr/include/glm)

