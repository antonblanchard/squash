add_executable (squash squash.c parg/parg.c)
target_add_extra_warning_flags (squash)
target_link_libraries (squash squash${SQUASH_VERSION_API})
target_include_directories (squash PRIVATE "${CMAKE_SOURCE_DIR}/squash")

install (TARGETS squash
  RUNTIME DESTINATION ${CMAKE_INSTALL_BINDIR})
