cmake_minimum_required(VERSION 3.20.0)
find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(smart_badge)

target_sources(app PRIVATE src/main.c  ../../mylib/ble_receive.c ../../mylib/hci.c)
include_directories(app PRIVATE ~/csse4011/project/mycode/include)