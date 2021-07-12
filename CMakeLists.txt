#
# ESP32 Crypto Component CMake
#

set (includes)
set (srcs)
set (priv_includes)
set (srcs_dirs)

list(APPEND includes
    "include"
    )

list(APPEND srcs
    "esp_crypto_libsodium.c"
    "esp_crypto_mbedtls.c"
    "esp_crypto.c"
    )

idf_component_register( SRCS "${srcs}"
                        INCLUDE_DIRS ${includes}
                        PRIV_INCLUDE_DIRS ${priv_includes}
                        REQUIRES mbedtls libsodium soc
                      )

# SRCS "${srcs}"
