SET(DGTAL_TOOLS_SRC
  estimatorComparator
  lengthEstimators
  vol2normalField
)

FOREACH(FILE ${DGTAL_TOOLS_SRC})
  add_executable(${FILE} ${FILE})
  target_link_libraries (${FILE}  ${DGTAL_LIBRARIES} )
  install(TARGETS ${FILE}
        RUNTIME DESTINATION bin
        LIBRARY DESTINATION lib
        ARCHIVE DESTINATION lib)
ENDFOREACH(FILE)

