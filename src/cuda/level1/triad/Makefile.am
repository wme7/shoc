if BUILD_MPI
    MAYBE_MPI = epmpi
endif
SUBDIRS = $(MAYBE_MPI)

include $(top_builddir)/config/config.mk
include $(top_builddir)/config/targets.mk

# How to find source files
VPATH = $(srcdir):$(srcdir)/../../common:$(srcdir)/../../../common

AM_LDFLAGS = $(CUDA_LDFLAGS)
AM_CPPFLAGS = $(CUDA_INC)

# What is the destination for programs built from this directory?
serialcudadir = $(bindir)/Serial/CUDA

# What programs should be installed to that destination?
serialcuda_PROGRAMS = Triad

# How to build those programs?
Triad_SOURCES = main.cpp
Triad_LDADD = Triad.o $(CUDA_LIBS) $(LIBS)

