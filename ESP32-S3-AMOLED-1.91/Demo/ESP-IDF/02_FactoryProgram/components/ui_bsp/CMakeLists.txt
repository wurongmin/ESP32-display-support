file(GLOB_RECURSE scrld ./*.c)
idf_component_register(
  SRCS ${scrld}
  REQUIRES lvgl
  INCLUDE_DIRS "custom" "generated" "generated/guider_customer_fonts")
target_compile_definitions(${COMPONENT_LIB} PUBLIC VersionControl_V2)