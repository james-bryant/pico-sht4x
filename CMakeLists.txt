add_library(pico_sht4x INTERFACE)

target_sources(pico_sht4x INTERFACE 
  ${CMAKE_CURRENT_LIST_DIR}/sensirion_common.c
  ${CMAKE_CURRENT_LIST_DIR}/sensirion_i2c_hal.c
  ${CMAKE_CURRENT_LIST_DIR}/sensirion_i2c.c
  ${CMAKE_CURRENT_LIST_DIR}/sht4x_i2c.c
)

target_include_directories(pico_sht4x INTERFACE ${CMAKE_CURRENT_LIST_DIR})

target_link_libraries(pico_sht4x INTERFACE i2c_bus_scan pico_stdlib hardware_i2c)