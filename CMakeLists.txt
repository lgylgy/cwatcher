cmake_minimum_required(VERSION 3.20)

project(CWatcher)

set(OATPP_BUILD_TESTS OFF)

set(CMAKE_CXX_STANDARD 20)
set(SOURCE_FILES src/main.cpp)

add_subdirectory(third_party/oatpp) 
include_directories(src)

add_executable(${PROJECT_NAME} ${SOURCE_FILES})
target_link_libraries(${PROJECT_NAME} PRIVATE oatpp)
