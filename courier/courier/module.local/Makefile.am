#
# Copyright 1998 - 2008 Double Precision, Inc.  See COPYING for
# distribution information.

CFLAGS=`cat cflags`


INCLUDES=`@COURIERAUTHCONFIG@ --cppflags`

BUILT_SOURCES=libexecdir.h modulelist.h sysconfdir.h
CLEANFILES=sysconfdir.h libexecdir.h modulelist.h module.local \
	permissions.dat
DISTCLEANFILES=cflags

moduledir=$(libexecdir)/courier/modules/local
globbindir=@prefix@/bin

sysconf_DATA=module.local

module.local: courier.config
	cp -f $(srcdir)/courier.config module.local

module_PROGRAMS=courierlocal courierdeliver

bin_PROGRAMS=preline

INSTALL=@INSTALL@ `test ! -w /etc || echo -o @mailuser@ -g @mailgroup@`
INSTALL_PROGRAM=${INSTALL} -m 555

EXTRA_DIST=courier.config testsuite testsuite.txt

courierlocal_SOURCES=localmail.c
courierlocal_DEPENDENCIES=../../courier/libs/libmodule.la \
			../../courier/libs/libcommon.la \
			../../courier/libs/libcourier.la \
			../../numlib/libnumlib.la \
			../../waitlib/libwaitlib.a

courierlocal_LDADD=../../courier/libs/libmodule.la \
			../../courier/libs/libcommon.la \
			../../courier/libs/libcourier.la \
			../../numlib/libnumlib.la \
			../../waitlib/libwaitlib.a

courierdeliver_SOURCES=deliver.c
courierdeliver_DEPENDENCIES=librewrite.la \
		../../courier/libs/libcommon.la \
		../../courier/libs/libcourier.la \
		../../maildir/libmaildir.la \
		../../rfc822/librfc822.la \
		../../liblock/liblock.la \
		../../waitlib/libwaitlib.a \
		../../numlib/libnumlib.la \
		../../unicode/libunicode.la

courierdeliver_LDADD=$(courierdeliver_DEPENDENCIES)

preline_SOURCES=preline.c

noinst_LTLIBRARIES=librewrite.la

install-data-hook:
	@test -w /etc || exit 0 ; cd $(DESTDIR)$(moduledir) || exit 1 ; chown @mailuser@ . ; chgrp @mailgroup@ .

install-perms:
	@$(MAKE) install-perms-recursive
	@$(MAKE) install-perms-local

install-perms-recursive:
	@>permissions.dat
	@SUBDIRS="$(SUBDIRS)" ; for f in $$SUBDIRS ; do ( cd $$f && $(MAKE) $(AM_MAKEFLAGS) install-perms ) ; cat /dev/null >>$$f/permissions.dat ; cat $$f/permissions.dat >>permissions.dat ; done

install-perms-local:
	@echo $(moduledir) 755 @mailuser@ @mailgroup@ >>permissions.dat
	@echo $(sysconfdir)/module.local 644 @mailuser@ @mailgroup@ config >>permissions.dat
	@echo $(moduledir)/courierlocal 755 @mailuser@ @mailgroup@ >>permissions.dat
	@echo $(moduledir)/courierdeliver 755 @mailuser@ @mailgroup@ >>permissions.dat
	@echo $(bindir)/preline 755 @mailuser@ @mailgroup@ >>permissions.dat

librewrite_la_SOURCES=local.c dotcourier.c
librewrite_la_LDFLAGS=-static

libexecdir.h: config.status
	echo "#define LIBEXECDIR \"$(libexecdir)\"" >libexecdir.h

modulelist.h: config.status
	echo "#define MODULELIST \"$(sysconfdir)/authmodulelist\"" >modulelist.h

sysconfdir.h: config.status
	echo "#define SYSCONFDIR \"$(sysconfdir)\"" >sysconfdir.h

check-am:
	$(srcdir)/testsuite | cmp -s - $(srcdir)/testsuite.txt
