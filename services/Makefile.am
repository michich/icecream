AM_CPPFLAGS = \
	-I$(top_srcdir)/minilzo

lib_LTLIBRARIES = libicecc.la
libicecc_la_SOURCES = job.cpp comm.cpp exitcode.cpp getifaddrs.cpp logging.cpp tempfile.c platform.cpp gcc.cpp
libicecc_la_LIBADD = \
	../minilzo/libminilzo.la \
	$(CAPNG_LDADD) \
	-ldl

libicecc_la_CFLAGS = -fPIC -DPIC
libicecc_la_CXXFLAGS = -fPIC -DPIC

icedir = $(includedir)/icecc
ice_HEADERS = \
	job.h \
	comm.h

noinst_HEADERS = \
	exitcode.h \
	getifaddrs.h \
	logging.h \
	tempfile.h \
	platform.h

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = icecc.pc
