# Add the patched SSD1322 driver into the build whenever
# CONFIG_SSD1322_PATCHED=y is selected.
if(CONFIG_SSD1322_PATCHED)
  zephyr_library_named(ssd1322_patched)
  zephyr_library_sources(${CMAKE_CURRENT_SOURCE_DIR}/drivers_patches/ssd1322.c)
endif()