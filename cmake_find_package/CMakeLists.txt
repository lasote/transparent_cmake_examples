PROJECT(myapp)
cmake_minimum_required(VERSION 3.1)
set(CMAKE_MODULE_PATH ${CMAKE_BINARY_DIR})

ADD_EXECUTABLE(myapp main.cpp)
find_package(libcurl)
target_link_libraries(myapp libcurl::libcurl)

