PROJECT(myapp)
cmake_minimum_required(VERSION 3.1)

add_definitions(-DCURL_STATICLIB)
ADD_EXECUTABLE(myapp main.cpp)

find_package(ZLIB)
find_package(OpenSSL)
find_package(CURL)

include_directories(${ZLIB_INCLUDE_DIRS} ${OPENSSL_INCLUDE_DIRS} ${CURL_INCLUDE_DIRS})
target_link_libraries(myapp ${CURL_LIBRARIES} ${OPENSSL_LIBRARIES} ${ZLIB_LIBRARIES} Ws2_32)

