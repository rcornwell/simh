## PDP1 simulator
##
## This is an automagically generated file. Do NOT EDIT.
## Any changes you make will be overwritten!!
##
## Make changes to the SIMH top-level makefile and then run the
## "cmake/generate.py" script to regenerate these files.
##
##     cd cmake; python -m generate --help
##
## ------------------------------------------------------------

if (HAVE_UNITY_FRAMEWORK AND EXISTS "${CMAKE_CURRENT_SOURCE_DIR}/unit-tests/CMakeLists.txt")
  add_subdirectory(unit-tests)
endif ()

add_simulator(pdp1
    SOURCES
        pdp1_lp.c
        pdp1_cpu.c
        pdp1_stddev.c
        pdp1_sys.c
        pdp1_dt.c
        pdp1_drm.c
        pdp1_clk.c
        pdp1_dcs.c
        pdp1_dpy.c
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}
    DEFINES
        DISPLAY_TYPE=DIS_TYPE30
        PIX_SCALE=RES_HALF
    FEATURE_VIDEO
    FEATURE_DISPLAY
    LABEL PDP1
    PKG_FAMILY decpdp_family
    TEST pdp1)
