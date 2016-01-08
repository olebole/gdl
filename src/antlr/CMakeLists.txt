aux_source_directory(${CMAKE_CURRENT_SOURCE_DIR} ANTLRSOURCES)
list(REMOVE_ITEM ANTLRSOURCES ${CMAKE_CURRENT_SOURCE_DIR}/dll.cpp)
include_directories(${CMAKE_SOURCE_DIR} ${CMAKE_SOURCE_DIR}/src/antlr)

add_library(gdl_antlr STATIC ${ANTLRSOURCES})
set_target_properties(gdl_antlr PROPERTIES POSITION_INDEPENDENT_CODE TRUE)
