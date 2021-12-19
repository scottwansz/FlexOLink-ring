# SPDX-License-Identifier: Apache-2.0

# zephyr_library()

# zephyr_library_sources(icm20948.c)
# zephyr_library_sources(icm20948_setup.c)
# zephyr_library_sources_ifdef(CONFIG_SPI icm20948_spi.c)
# zephyr_library_sources_ifdef(CONFIG_ICM20948_TRIGGER icm20948_trigger.c)

if(CONFIG_ICM20948)
  # Add *.h to the set of global include paths.
  zephyr_include_directories(.)

  zephyr_library()

  zephyr_library_sources(icm20948.c)
  zephyr_library_sources(icm20948_setup.c)
  zephyr_library_sources_ifdef(CONFIG_SPI icm20948_spi.c)
  zephyr_library_sources_ifdef(CONFIG_ICM20948_TRIGGER icm20948_trigger.c)
endif()
