sdk_add_include_directories(btble_inc)
sdk_add_include_directories(btblecontroller_port)

# use default port built by lib
#target_sources(app PRIVATE btblecontroller_port/btblecontroller_port_os.c)
#target_sources(app PRIVATE btblecontroller_port/btblecontroller_port.c)
#target_sources(app PRIVATE btblecontroller_port/btblecontroller_port_uart.c)

if("${PRIV_CONFIG_GEN_BLE}" STREQUAL "ble1m0s1bredr0" AND "${CHIP}" STREQUAL "bl616")
sdk_add_static_library(lib/libbtblecontroller_bl616_ble1m0s1bredr0.a)
endif()