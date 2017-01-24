## Process this file with automake to produce Makefile.in

## Created by Anjuta


uidir = $(pkgdatadir)/ui
ui_DATA = pwstore.ui


AM_CPPFLAGS = \
	-DPACKAGE_LOCALE_DIR=\""$(localedir)"\" \
	-DPACKAGE_SRC_DIR=\""$(srcdir)"\" \
	-DPACKAGE_DATA_DIR=\""$(pkgdatadir)"\" \
	$(PWSTORE_CFLAGS)

AM_CFLAGS =\
	 -Wall\
	 -g

bin_PROGRAMS = pwstore

pwstore_SOURCES = \
	pwstore.vala config.vapi

pwstore_VALAFLAGS =  \
	--pkg gtk+-3.0


pwstore_LDFLAGS =

pwstore_LDADD = $(PWSTORE_LIBS)


if PLATFORM_WIN32
pwstore_LDFLAGS += -Wl,--export-all-symbols
else
pwstore_LDFLAGS += -Wl,--export-dynamic
endif

if NATIVE_WIN32
pwstore_LDFLAGS += -mwindows
endif


EXTRA_DIST = $(ui_DATA)

# Remove ui directory on uninstall
uninstall-local:
	-rm -r $(uidir)
	-rm -r $(pkgdatadir)

