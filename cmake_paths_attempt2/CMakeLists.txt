PROJECT(myapp)
cmake_minimum_required(VERSION 3.1)

ADD_EXECUTABLE(myapp main.cpp)

find_package(ZLIB)
if(ZLIB_FOUND)
  include_directories(${ZLIB_INCLUDE_DIRS})
  target_link_libraries(myapp ${ZLIB_LIBRARIES})
endif()

find_package(OpenSSL)
if(OpenSSL_FOUND)
  include_directories(${OpenSSL_INCLUDE_DIRS})
  target_link_libraries(myapp ${OpenSSL_LIBRARIES})
endif()

find_package(CURL)
if(CURL_FOUND)
   include_directories(${CURL_INCLUDE_DIRS})
   target_link_libraries(myapp ${CURL_LIBRARIES})
endif()