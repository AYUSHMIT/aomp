NOOPT        = 1
include ../../Makefile.defs
OMP_FLAGS    += -O3 -save-temps

TESTNAME     = flang-485265
TESTSRC_MAIN = flang-485265.f90
TESTSRC_AUX  =
TESTSRC_ALL  = $(TESTSRC_MAIN) $(TESTSRC_AUX)

FLANG        ?= flang-new
OMP_BIN      = $(AOMP)/bin/$(FLANG)
CC           = $(OMP_BIN) $(VERBOSE)
#-ccc-print-phases
#"-\#\#\#"

RUNENV       = AOMP_GPU=${AOMP_GPU}
RUNCMD       = ./chkit.sh

include ../Makefile.rules
