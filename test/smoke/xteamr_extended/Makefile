include ../../Makefile.defs

TESTNAME     = test_xteamr
TESTSRC_MAIN = test_xteamr.cpp
TESTSRC_AUX  =
TESTSRC_ALL  = $(TESTSRC_MAIN) $(TESTSRC_AUX)

CLANG        ?= clang++
OMP_BIN      = $(AOMP)/bin/$(CLANG)
CC           = $(OMP_BIN) $(VERBOSE)

CFLAGS       = -O3 -std=c++11 -fopenmp-target-fast
ifneq ("$(wildcard $(AOMP)/lib/libmlir_float16_utils.so)","")
  CFLAGS += -lmlir_float16_utils
endif
#-ccc-print-phases
#"-\#\#\#"


ifeq ($(ISVIRT),1)
ARGS = $(GPU_MEM_SIZE_GIB)
endif

UNSUPPORTED = ASAN_COMPILE

include ../Makefile.rules
