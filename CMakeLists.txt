cmake_minimum_required(VERSION 3.6)
project(AsioTcpServer)

set(CMAKE_CXX_STANDARD 11)

set(SOURCE_FILES main.cpp server_base.hpp server_http.hpp handler.hpp)

include_directories(/usr/include/boost)
link_directories(/usr/lib/x86_64-linux-gnu)

add_executable(AsioTcpServer ${SOURCE_FILES})

target_link_libraries(AsioTcpServer pthread)
target_link_libraries(AsioTcpServer boost_system)
