add_subdirectory(crossgen)
if (CLR_CMAKE_TARGET_WIN32 AND NOT CLR_CMAKE_CROSS_ARCH)
  add_subdirectory(GenClrDebugResource)
  add_subdirectory(InjectResource)

  if (CLR_CROSS_COMPONENTS_BUILD)
    install(EXPORT dactabletools DESTINATION dactabletools)
  endif()
endif()
