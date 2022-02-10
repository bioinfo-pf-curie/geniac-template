include(ExternalProject)

###########################################################################
# Only modify the section below
###########################################################################
### BEGIN >>> ExternalProject section
ExternalProject_Add(
    helloWorld
    SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR}/helloWorld
    CMAKE_ARGS
    -DCMAKE_INSTALL_PREFIX=${CMAKE_BINARY_DIR}/externalProject/bin)

### END >>> ExternalProject section
###########################################################################


###########################################################################
# the code below should not be modified
###########################################################################

# IMPORTANT: DESTINATION for install must always be ${CMAKE_INSTALL_PREFIX}/${pipeline_dir}/bin/fromSource
install(
    DIRECTORY ${CMAKE_BINARY_DIR}/externalProject/bin/
    DESTINATION ${CMAKE_INSTALL_PREFIX}/${pipeline_dir}/bin/fromSource
    USE_SOURCE_PERMISSIONS)

