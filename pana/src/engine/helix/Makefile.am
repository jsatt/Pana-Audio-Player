kde_module_LTLIBRARIES = \
    libpana_helixengine_plugin.la

SUBDIRS = \
    helix-sp \
    config

INCLUDES = \
    -I$(top_srcdir)/pana/src \
    -I$(top_builddir)/pana/src/panacore \
    $(all_includes)

AM_CPPFLAGS = \
    -D_UNIX \
    -Wall -Wreturn-type \
    -fno-exceptions \
    -I$(top_srcdir)/pana/src/engine/helix/helix-sp \
    -I$(top_srcdir)/pana/src/engine/helix/config \
    -I$(top_srcdir)/pana/src/ \
    -include $(top_srcdir)/pana/src/engine/helix/helix-sp/helixdefines.h \
    $(all_includes)

libpana_helixengine_plugin_la_SOURCES = \
    helix-engine.cpp \
    helix-errors.cpp \
    helix-configdialog.cpp \
    hxplayercontrol.cpp

libpana_helixengine_plugin_la_LIBADD = \
    $(top_builddir)/pana/src/libpana.la \
    $(top_builddir)/pana/src/engine/helix/helix-sp/libhelix-sp.la \
    $(top_builddir)/pana/src/engine/helix/config/libhelixconfig.la \
    $(top_builddir)/pana/src/plugin/libplugin.la \
    -lkdeui -lkdecore $(ALSALIB_LIBS)

libpana_helixengine_plugin_la_LDFLAGS = -module $(KDE_PLUGIN) $(all_libraries)

METASOURCES = \
    AUTO

kde_services_DATA = \
    pana_helixengine_plugin.desktop

KDE_OPTIONS=nofinal
