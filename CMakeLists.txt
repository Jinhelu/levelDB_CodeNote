cmake_minimum_required (VERSION 2.8)
project(test_leveldb)


# 设置包含的目录
include_directories(
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${CMAKE_CURRENT_BINARY_DIR}
    ${CMAKE_CURRENT_SOURCE_DIR}/include
)
# 设置链接库搜索目录
link_directories(
    /usr/local/lib
)

add_executable(test main.cpp)

# 设置可执行文件需要链接的库
target_link_libraries(test
    -lleveldb
    -lpthread
)