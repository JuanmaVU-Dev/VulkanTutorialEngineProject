cmake_minimum_required(VERSION 3.28)
project(untitled)

set(CMAKE_CXX_STANDARD 23)
find_package(Vulkan REQUIRED)
add_executable(untitled main.cpp)

include_directories(C:\\VulkanSDK\\1.3.283.0\\Include)
include_directories(glm)
include_directories(glfw-3.4.bin.WIN64/include)

target_link_libraries(untitled PRIVATE Vulkan::Vulkan)

#### INCLUDE LIBRARIES ####
include_directories(lib)
# Include GLFW library
add_subdirectory(lib/glfw-3.4)

target_link_libraries(untitled PRIVATE glfw)