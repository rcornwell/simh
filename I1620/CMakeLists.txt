## I1620 simulator
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

add_simulator(i1620
    SOURCES
        i1620_cd.c
        i1620_dp.c
        i1620_pt.c
        i1620_tty.c
        i1620_cpu.c
        i1620_lp.c
        i1620_fp.c
        i1620_sys.c
    INCLUDES
        ${CMAKE_CURRENT_SOURCE_DIR}
    LABEL I1620
    PKG_FAMILY ibm_family
    TEST i1620)
