SET(LOCAL_FILES
    lineGraph.png
    transformation.png
    original.png
    )

foreach (f ${LOCAL_FILES})
    configure_file(${f} "${PGR_DOCUMENTATION_SOURCE_DIR}/images/${f}" COPYONLY)
    list(APPEND LOCAL_IMG_FILES  "${PGR_DOCUMENTATION_SOURCE_DIR}/images/${f}")
endforeach()

set(PGROUTING_IMG_FILES ${PGROUTING_IMG_FILES} ${LOCAL_IMG_FILES} PARENT_SCOPE)
