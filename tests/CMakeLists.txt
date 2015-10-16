include_directories(${CMAKE_CURRENT_SOURCE_DIR}/..)

find_package(Check REQUIRED)
include_directories(${CHECK_INCLUDE_DIRS})

set(LIBS addrwatch ${CHECK_LIBRARIES} m rt pthread)

add_executable(check_addrwatch check_addrwatch.c config.h)
target_link_libraries(check_addrwatch ${LIBS})
