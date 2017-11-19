cmake_minimum_required(VERSION 3.5)

project(OpenSceneGraph-Tutorials VERSION 3.4)

# Find OpenSceneGraph
set(OSG_DIR $ENV{OSG_DIR} CACHE PATH "Path where to find the OpenSceneGraph")

find_package(OpenSceneGraph 3.4.0 REQUIRED osgGA osgDB osgViewer)

# Find Third Party Libraries
set(OSG_THIRD_PARTY_DIR $ENV{OSG_3RDPARTY_DIR} CACHE PATH "Path where to find the osg third party dependencies")

if(MSVC_VERSION EQUAL 1600 OR MSVC_VERSION GREATER 1600)
  set(USERFILE_ENVIRONMENT_DEBUG "PATH=${OSG_DIR}/bin;${OSG_THIRD_PARTY_DIR}/bin")

endif()

# Add tutorials
add_subdirectory(basic_geometry)

