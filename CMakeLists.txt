#
# Copyright 2024 NXP
#
# SPDX-License-Identifier: MIT
#


if(CONFIG_MCUX_COMPONENT_middleware.aws_iot.ota)
    mcux_add_source(
        SOURCES source/ota.c
                source/ota_base64.c
                source/ota_cbor.c
                source/ota_http.c
                source/ota_interface.c
                source/ota_mqtt.c
                source/include/ota.h
                source/include/ota_appversion32.h
                source/include/ota_base64_private.h
                source/include/ota_cbor_private.h
                source/include/ota_config_defaults.h
                source/include/ota_http_interface.h
                source/include/ota_http_private.h
                source/include/ota_interface_private.h
                source/include/ota_mqtt_interface.h
                source/include/ota_mqtt_private.h
                source/include/ota_os_interface.h
                source/include/ota_platform_interface.h
                source/include/ota_private.h
                source/include/stdbool.readme
                source/include/stdint.readme
    )
    mcux_add_include(
        INCLUDES source/include
    )
endif()

if(CONFIG_MCUX_COMPONENT_middleware.aws_iot.ota.freertos)
    mcux_add_source(
        SOURCES source/portable/os/ota_os_freertos.c
                source/portable/os/ota_os_freertos.h
    )
    mcux_add_include(
        INCLUDES source/portable/os
    )
endif()
