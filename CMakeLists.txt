cmake_minimum_required(VERSION 3.3)
project(awsv4_cpp)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")

find_package(OpenSSL REQUIRED)

include_directories(${OPENSSL_INCLUDE_DIR})

set(SOURCE_FILES
    awsv4.cpp
    awsv4.hpp
    main.cpp)

add_executable(awsv4_cpp ${SOURCE_FILES})
target_link_libraries(awsv4_cpp ${OPENSSL_LIBRARIES} PocoFoundation PocoNet)
