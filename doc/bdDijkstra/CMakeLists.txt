
SET(LOCAL_FILES
    bdDijkstra-family.rst
    pgr_bdDijkstraCost.rst
    pgr_bdDijkstraCostMatrix.rst
    pgr_bdDijkstra.rst
    )

foreach (f ${LOCAL_FILES})
    configure_file(${f} "${PGR_DOCUMENTATION_SOURCE_DIR}/${f}")
    list(APPEND LOCAL_DOC_FILES  ${PGR_DOCUMENTATION_SOURCE_DIR}/${f})
endforeach()

set(PGROUTING_DOC_FILES ${PGROUTING_DOC_FILES} ${LOCAL_DOC_FILES} PARENT_SCOPE)

