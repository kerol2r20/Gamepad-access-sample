project(GamepadAPI)
cmake_minimum_required(VERSION 3.0)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(libevdev)

add_executable(main main.c)

include_directories(${LIBEVDEV_INCLUDE_DIRS})
target_link_libraries(main evdev)
