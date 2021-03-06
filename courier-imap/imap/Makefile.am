#
# Copyright 1998 - 2008 Double Precision, Inc.  See COPYING for
# distribution information.

INCLUDES=@CPPAUTH@

BUILT_SOURCES=README.proxy

CONFIG_STATUS_DEPENDENCIES = ../tcpd/couriertls.config

DISTCLEANFILES=imapd.pam pop3d.pam imapd.cnf pop3d.cnf
CLEANFILES=imapd.8 imapd.html mkimapdcert.html mkimapdcert.8 \
	courierpop3d.html courierpop3d.8 mkpop3dcert.html mkpop3dcert.8

EXTRA_DIST=testsuite testsuite.txt smaptestsuite smaptestsuite.txt \
	BUGS BUGS.html README README.html imapd.authpam \
	pop3d.authpam system-auth.authpam system-auth2.authpam\
	imapd.html.in imapd.8.in \
	mkimapdcert.html.in mkimapdcert.8.in \
	mkpop3dcert.html.in mkpop3dcert.8.in \
	courierpop3d.html.in courierpop3d.8.in \
	README.proxy README.proxy.html \
	imapd.cnf.gnutls pop3d.cnf.gnutls

noinst_SCRIPTS=mkimapdcert mkpop3dcert
noinst_PROGRAMS=imaplogin imapd pop3login pop3d

noinst_DATA=imapd.8 imapd.html imapd.cnf pop3d.cnf \
	mkimapdcert.html mkimapdcert.8 \
	mkpop3dcert.html mkpop3dcert.8 \
	courierpop3d.html courierpop3d.8

imapd.cnf: imapd.cnf.@ssllib@
	cp imapd.cnf.@ssllib@ imapd.cnf
	touch imapd.cnf

imapd.cnf: $(top_builddir)/config.status

pop3d.cnf: pop3d.cnf.@ssllib@
	cp pop3d.cnf.@ssllib@ pop3d.cnf
	touch pop3d.cnf

pop3d.cnf: $(top_builddir)/config.status

noinst_LTLIBRARIES=libimaplogin.la libimapd.la libpop3d.la
libimaplogin_la_SOURCES=
libimaplogin_la_LIBADD=../tcpd/libspipe.la ../tcpd/libtlsclient.la \
	../numlib/libnumlib.la
libimaplogin_la_LDFLAGS=-static

libimapd_la_SOURCES=mainloop.c imaptoken.c imaptoken.h imapwrite.c \
	imapwrite.h capability.c externalauth.c smap.c smapsnapshot.c
libimapd_la_LIBADD= ../rfc2045/librfc2045.la ../maildir/libmaildir.la \
	../rfc822/librfc822.la ../liblock/liblock.la ../numlib/libnumlib.la \
	../unicode/libunicode.la
libimapd_la_LDFLAGS=-static

imaplogin_SOURCES=imaplogin.c authenticate_auth.c proxy.c proxy.h
imaplogin_DEPENDENCIES=libimapd.la libimaplogin.la
imaplogin_LDADD=libimapd.la libimaplogin.la \
	@LDAUTH@ -lcourierauth -lcourierauthsasl

imapd_SOURCES=fetch.c fetchinfo.c fetchinfo.h imapd.c imapd.h \
	imapscanclient.c imapscanclient.h \
	mailboxlist.c mailboxlist.h \
	msgbodystructure.c msgenvelope.c \
	mysignal.c mysignal.h \
	outbox.c outbox.h \
	thread.c thread.h \
	search.c searchinfo.c searchinfo.h \
	storeinfo.c storeinfo.h

imapd_DEPENDENCIES=libimapd.la \
	../maildir/maildir.libdeps @dblibrary@

imapd_LDADD=libimapd.la `cat ../maildir/maildir.libdeps` \
	@dblibrary@ @DEBUGLIB@ @LDAUTH@ -lcourierauth

pop3login_SOURCES=pop3login.c pop3dcapa.c proxy.c proxy.h
pop3login_DEPENDENCIES=../tcpd/libspipe.la ../tcpd/libspipe.la libpop3d.la
pop3login_LDADD=../tcpd/libtlsclient.la ../tcpd/libspipe.la libpop3d.la ../tcpd/libspipe.la @LDAUTH@ -lcourierauth -lcourierauthsasl @NETLIBS@

libpop3d_la_SOURCES=externalauth.c
libpop3d_la_LIBADD=../maildir/libmaildir.la ../rfc822/librfc822.la \
	../numlib/libnumlib.la
libpop3d_la_DEPENDENCIES=$(libpop3d_la_LIBADD)
libpop3d_la_LDFLAGS=-static

pop3d_SOURCES=pop3dserver.c pop3dcapa.c
pop3d_DEPENDENCIES=libpop3d.la
pop3d_LDADD=libpop3d.la @LDAUTH@ -lcourierauth

HTML2TXT=links -dump -no-numbering

README: README.html
	$(HTML2TXT) README.html >README

BUGS: BUGS.html
	$(HTML2TXT) BUGS.html >BUGS

imapd.html: imapd.html.in
	./config.status --file=imapd.html

imapd.8: imapd.8.in
	./config.status --file=imapd.8

mkimapdcert.html: mkimapdcert.html.in
	./config.status --file=mkimapdcert.html

mkimapdcert.8: mkimapdcert.8.in
	./config.status --file=mkimapdcert.8

mkpop3dcert.html: mkpop3dcert.html.in
	./config.status --file=mkpop3dcert.html

mkpop3dcert.8: mkpop3dcert.8.in
	./config.status --file=mkpop3dcert.8

courierpop3d.html: courierpop3d.html.in
	./config.status --file=courierpop3d.html

courierpop3d.8: courierpop3d.8.in
	./config.status --file=courierpop3d.8

if HAVE_SGML
imapd.html.in: imapd.sgml ../docbook/sgml2html
	../docbook/sgml2html imapd.sgml imapd.html.in

imapd.8.in: imapd.sgml ../docbook/sgml2man
	../docbook/sgml2man imapd.sgml imapd.8.in
	mv imapd.8 imapd.8.in

mkimapdcert.html.in: mkimapdcert.sgml ../docbook/sgml2html
	../docbook/sgml2html mkimapdcert.sgml mkimapdcert.html.in

mkimapdcert.8.in: mkimapdcert.sgml ../docbook/sgml2man
	../docbook/sgml2man mkimapdcert.sgml mkimapdcert.8.in
	mv mkimapdcert.8 mkimapdcert.8.in

mkpop3dcert.html.in: mkpop3dcert.sgml ../docbook/sgml2html
	../docbook/sgml2html mkpop3dcert.sgml mkpop3dcert.html.in

mkpop3dcert.8.in: mkpop3dcert.sgml ../docbook/sgml2man
	../docbook/sgml2man mkpop3dcert.sgml mkpop3dcert.8.in
	mv mkpop3dcert.8 mkpop3dcert.8.in

courierpop3d.html.in: courierpop3d.sgml ../docbook/sgml2html
	../docbook/sgml2html courierpop3d.sgml courierpop3d.html.in

courierpop3d.8.in: courierpop3d.sgml ../docbook/sgml2man
	../docbook/sgml2man courierpop3d.sgml courierpop3d.8.in
	mv courierpop3d.8 courierpop3d.8.in

README.proxy.html: README.proxy.sgml ../docbook/sgml2html
	../docbook/sgml2html README.proxy.sgml README.proxy.html

README.proxy: README.proxy.html
	$(HTML2TXT) README.proxy.html >README.proxy
endif

check-am:
	@test "@MAKECHECKBROKEN@" = "Y" || exit 0; echo "" ; echo "Error: --with-trashquota or the --enable-workarounds-for-imap-client-bugs" ; echo "option was specified to the configure script."; echo ""; echo "As INSTALL told you, make check fails if these options are used, and I wasn't"; echo "kidding when I wrote it.  Reconfigure and rebuild without these options, then"; echo "rerun make and make check.  If make check passes, reconfigure again with your"; echo "original options, and proceed with installing this server.  Have fun!"; exit 1
	@cp /dev/null conftest1 ; chmod 000 conftest1 ; test -w conftest1 || \
		exit 0; echo "=============================" ; \
		echo "Do not run make check as root" ; \
		echo "=============================" ; exit 1
	@rm -f conftest1
	@chmod +x testsuitefix.pl
	LC_ALL=C; export LC_ALL; $(srcdir)/testsuite | ./testsuitefix.pl | sort | cmp -s - $(srcdir)/testsuite.txt
	LC_ALL=C; export LC_ALL; test "@smap@" = "yes" || exit 0; @SHELL@ $(srcdir)/smaptestsuite | ./testsuitefix.pl | sort | cmp -s - $(srcdir)/smaptestsuite.txt
	rm -rf confmdtest

testsuite-imap:
	@LC_ALL=C; export LC_ALL; $(srcdir)/testsuite | ./testsuitefix.pl | sort

testsuite-smap:
	@LC_ALL=C; export LC_ALL; test "@smap@" = "yes" || exit 0; @SHELL@ $(srcdir)/smaptestsuite | ./testsuitefix.pl | sort
