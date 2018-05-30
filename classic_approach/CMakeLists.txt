PROJECT(myapp)
cmake_minimum_required(VERSION 3.1)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
CONAN_BASIC_SETUP(TARGETS)

ADD_EXECUTABLE(myapp main.cpp)
target_link_libraries(myapp CONAN_PKG::libcurl)

