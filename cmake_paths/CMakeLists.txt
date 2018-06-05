PROJECT(myapp)
cmake_minimum_required(VERSION 3.1)

ADD_EXECUTABLE(myapp main.cpp)
find_package(CURL)
include_directories(${CURL_INCLUDE_DIRS})
target_link_libraries(myapp ${CURL_LIBRARIES})

