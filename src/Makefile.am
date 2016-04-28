AUTOMAKE_OPTIONS=foreign

SUBDIRS = test

AM_CPPFLAGS = -DCONFIG_FILE=\"${sysconfdir}/udiRoot.conf\" -DLIBEXECDIR=\"${libexecdir}/shifter\" -Wall

sbin_PROGRAMS = setupRoot unsetupRoot
bin_PROGRAMS = shifter shifterimg

SHIFTER_SOURCES = \
    shifter.c \
    UdiRootConfig.c \
    utility.c \
    config.h \
    shifter_core.c \
    ImageData.c \
    VolumeMap.c \
    MountList.c

SETUPROOT_SOURCES = \
    setupRoot.c \
    UdiRootConfig.c \
    utility.c \
    config.h \
    shifter_core.c \
    ImageData.c \
    VolumeMap.c \
    MountList.c

UNSETUPROOT_SOURCES = \
    unsetupRoot.c \
    UdiRootConfig.c \
    utility.c \
    config.h \
    shifter_core.c \
    ImageData.c \
    VolumeMap.c \
    MountList.c

SHIFTERIMG_SOURCES = \
    shifterimg.c \
    ImageData.c \
    utility.c \
    UdiRootConfig.c \
	VolumeMap.c


shifter_SOURCES = $(SHIFTER_SOURCES)
setupRoot_SOURCES = $(SETUPROOT_SOURCES)
unsetupRoot_SOURCES = $(UNSETUPROOT_SOURCES)
shifterimg_SOURCES = $(SHIFTERIMG_SOURCES)
shifterimg_LDFLAGS = $(MUNGE_LDFLAGS) $(JSON_LDFLAGS) $(LIBCURL) $(MUNGE_LDFLAGS)
shifterimg_CPPFLAGS = $(AM_CPPFLAGS) $(MUNGE_CPPFLAGS) $(JSON_CPPFLAGS) $(LIBCURL_CPPFLAGS) $(MUNGE_CPPFLAGS)

install-data-hook:
	/bin/chmod 4755 $(DESTDIR)/$(bindir)/shifter