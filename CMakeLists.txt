cmake_minimum_required (VERSION 3.13)
project(MAX6675)

add_executable(max6675 max6675.c)

# Locate libraries and headers
find_package(WiringPi REQUIRED)
find_package(Threads REQUIRED)

# Include headers
include_directories(${WIRINGPI_INCLUDE_DIRS})
target_link_libraries(max6675 ${WIRINGPI_LIBRARIES})
target_link_libraries(max6675 ${CMAKE_THREAD_LIBS_INIT})


