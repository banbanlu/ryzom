FILE(GLOB SRC *.cpp *.h)

ADD_EXECUTABLE(ig_elevation ${SRC})

INCLUDE_DIRECTORIES(${LIBXML2_INCLUDE_DIR})

TARGET_LINK_LIBRARIES(ig_elevation nelmisc nel3d nelligo)
NL_DEFAULT_PROPS(ig_elevation "NeL, Tools, 3D: ig_elevation")
NL_ADD_RUNTIME_FLAGS(ig_elevation)

ADD_DEFINITIONS(${LIBXML2_DEFINITIONS})

INSTALL(TARGETS ig_elevation RUNTIME DESTINATION ${NL_BIN_PREFIX} COMPONENT tools3d)
