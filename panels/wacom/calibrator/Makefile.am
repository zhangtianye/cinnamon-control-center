# This is used in PANEL_CFLAGS
cappletname = wacom

AM_CPPFLAGS = 						\
	$(PANEL_CFLAGS)					\
	$(WACOM_PANEL_CFLAGS)				\
	-DCINNAMONLOCALEDIR="\"$(datadir)/locale\""	\
	$(NULL)


noinst_LTLIBRARIES = libwacom-calibrator.la

libwacom_calibrator_la_SOURCES =	\
	calibrator.c			\
	calibrator.h			\
	gui_gtk.c			\
	gui_gtk.h

libwacom_calibrator_la_LIBADD = $(PANEL_LIBS) $(WACOM_PANEL_LIBS)
libwacom_calibrator_la_LDFLAGS = $(WARN_LDFLAGS) $(PANEL_LDFLAGS)

noinst_PROGRAMS = test-calibrator

test_calibrator_SOURCES =		\
	main.c				\
	calibrator.c			\
	calibrator.h			\
	gui_gtk.c			\
	gui_gtk.h

test_calibrator_CFLAGS = $(AM_CFLAGS)
test_calibrator_LDADD = $(PANEL_LIBS) $(WACOM_PANEL_LIBS)

-include $(top_srcdir)/git.mk
