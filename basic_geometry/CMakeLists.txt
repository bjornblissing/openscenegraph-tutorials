add_executable(basic_geometry basic_geometry.cpp)

# Include the relevant OSG libraries
target_link_libraries(basic_geometry PRIVATE
  optimized ${OPENTHREADS_LIBRARY}
  optimized ${OSG_LIBRARY}
  optimized ${OSGVIEWER_LIBRARY}
  debug ${OPENTHREADS_LIBRARY_DEBUG}
  debug ${OSG_LIBRARY_DEBUG}
  debug ${OSGVIEWER_LIBRARY_DEBUG}
)

target_include_directories(basic_geometry PRIVATE
  ${OPENSCENEGRAPH_INCLUDE_DIRS}
)

# Needed to set the correct environment so that Visual Studio can 
# find the relevant dll files needed to run the project
if(MSVC_VERSION EQUAL 1600 OR MSVC_VERSION GREATER 1600)
  configure_file(../visual_studio_template/userfile.vcxproj.template basic_geometry.vcxproj.user @ONLY)
endif()