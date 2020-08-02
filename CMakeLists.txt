if(CONFIG_JSONC)
zephyr_interface_library_named(JSONC)

#target_include_directories(JSONC INTERFACE .)

zephyr_include_directories(.)

zephyr_library()
zephyr_library_sources(
	arraylist.c
	debug.c
	json_c_version.c
	json_object.c
	json_object_iterator.c
	json_pointer.c
	json_tokener.c
	json_util.c
	json_visit.c
	libjson.c
	linkhash.c
	printbuf.c
	random_seed.c
	strerror_override.c
)

zephyr_library_link_libraries(JSONC)
target_link_libraries(JSONC INTERFACE zephyr_interface)
endif()
