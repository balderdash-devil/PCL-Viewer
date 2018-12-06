file(GLOB pclviewer_src
    "*.h"
    "*.cpp"
)


# static library
add_library(pclviewer_static STATIC ${pclviewer_src})
target_link_libraries( pclviewer_static ${GLEW_LIBRARIES} )

add_library(pclviewer_shared SHARED ${pclviewer_src})
target_link_libraries( pclviewer_shared ${GLEW_LIBRARIES} )
add_subdirectory(main)

# install libs
# install(TARGETS example_static DESTINATION example/lib)
# install(TARGETS example_shared DESTINATION example/lib)

# install headers
# install(FILES ${PROJECT_SOURCE_DIR}/src/FooBar.h DESTINATION example/include)