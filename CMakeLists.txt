file(GLOB sources_vart *.c)
file(GLOB headers_vart *.h)

add_library(vart ${sources_vart} ${headers_vart})
add_dependencies(vart varuna)
install(TARGETS vart DESTINATION lib)
