noinst_LTLIBRARIES = libauthentication.la

INCLUDES = \
  -I$(top_srcdir)/pana/src \
  -I$(top_srcdir)/pana/src/panacore \
  -I$(top_srcdir)/pana/src/mediadevice \
  -I$(top_srcdir)/pana/src/mediadevice/daap \
  -I$(top_srcdir)/pana/src/mediadevice/daap/daapreader \
  $(all_includes)

libauthentication_la_SOURCES = contentfetcher.cpp md5.c hasher.c

libauthentication_la_LIBADD = \
   $(LIB_QT) \
   $(LIB_KDECORE) \
   $(LIB_KDEUI)

libauthentication_la_LDFLAGS = $(all_libraries) $(KDE_RPATH)

METASOURCES = AUTO

noinst_HEADERS = contentfetcher.h md5.h hasher.h portability.h
