#
# Copyright 1998 - 2009 Double Precision, Inc.  See COPYING for
# distribution information.


INCLUDES=@AUTHINCLUDE@

DISTCLEANFILES=uidgid testmailbot.*
CLEANFILES=maildrop.html maildrop.1 maildropfilter.7 maildropfilter.html

DBLIB=@dblibrary@

BUILT_SOURCES=	maildrop.html.in maildrop.1.in \
		maildropfilter.html.in maildropfilter.7.in \
		maildropgdbm.html maildropgdbm.7 \
		maildropex.html maildropex.7 \
		makedat.html makedat.1 \
		mailbot.html mailbot.1 \
		reformail.html reformail.1

noinst_LTLIBRARIES = libmdcommon.la


libmdcommon_la_SOURCES=alarm.C alarm.h alarmsleep.C alarmsleep.h alarmtimer.C \
	alarmtimer.h buffer.C buffer.h dotlock.C dotlock.h \
	dotlockrefresh.C dotlockrefresh.h exittrap.C exittrap.h funcs.C \
	funcs.h maildrop.C maildrop.h mio.C mio.h setgroupid.c setgroupid.h \
	tempfile.C tempfile.h
libmdcommon_la_LIBADD=../maildir/libmaildir.la \
	../rfc822/librfc822.la \
	../unicode/libunicode.la \
	../numlib/libnumlib.la ../liblock/liblock.la \
	$(DBLIB)
libmdcommon_la_LDFLAGS=-static


maildrop_SOURCES=deliver.C deliverdotlock.C deliverdotlock.h \
	dotlockmaildrop.C filelock.C filelock.h filter.C formatmbox.C \
	formatmbox.h globaltimer.C globaltimer.h lexer.C lexer.h log.C log.h \
	maildir.C maildir.h main.C message.C message.h messageinfo.C \
	messageinfo.h mytime.h mywait.h pipefds.C pipefds.h re.C re.h \
	recipe.C recipe.h recipenode.C recipenode.h recipeparse.C reeval.C \
	reeval.h regexpnode.h rematch.C rematch.h rematchmsg.C rematchmsg.h \
	rematchstr.C rematchstr.h search.C search.h token.C \
	token.h varlist.C varlist.h

maildrop_DEPENDENCIES = libmdcommon.la ../maildir/maildir.libdeps

maildrop_LDADD = libmdcommon.la `cat ../maildir/maildir.libdeps`\
	@AUTHLDADD@ -lpcre
maildrop_LDFLAGS=

reformail_SOURCES=reformail.C
reformail_LDADD = libmdcommon.la
reformail_DEPENDENCIES = $(reformail_LDADD)

noinst_PROGRAMS=maildrop reformail mailbot

mailbot_SOURCES=mailbot.c
mailbot_DEPENDENCIES=../rfc2045/librfc2045.la \
	../rfc822/librfc822.la ../liblock/liblock.la \
	../numlib/libnumlib.la ../unicode/libunicode.la $(DBLIB)
mailbot_LDADD=../rfc2045/librfc2045.la \
	../rfc822/librfc822.la ../liblock/liblock.la \
	../numlib/libnumlib.la ../unicode/libunicode.la $(DBLIB)
mailbot_LDFLAGS = -static

if HAVE_LIBIDN
TESTSUITE=testsuite.txt.idn
else
TESTSUITE=testsuite.txt.noidn
endif

EXTRA_DIST = maildroptips.html $(BUILT_SOURCES)\
	maildrop.lsm testsuite.txt.idn testsuite.txt.noidn

check-am:
	@chmod +x testsuite
	./testsuite | cmp -s - $(srcdir)/$(TESTSUITE)

noinst_DATA=maildrop.html maildrop.1 maildropfilter.html maildropfilter.7 \
	maildropgdbm.html maildropgdbm.7

if HAVE_SGML
maildrop.html.in: maildrop.sgml ../docbook/sgml2html
	../docbook/sgml2html maildrop.sgml maildrop.html.in

maildrop.1.in: maildrop.sgml ../docbook/sgml2man
	../docbook/sgml2man maildrop.sgml maildrop.1.in
	mv maildrop.1 maildrop.1.in

maildropfilter.html.in: maildropfilter.sgml ../docbook/sgml2html
	../docbook/sgml2html maildropfilter.sgml maildropfilter.html.in

maildropfilter.7.in: maildropfilter.sgml ../docbook/sgml2html
	../docbook/sgml2man maildropfilter.sgml maildropfilter.7.in
	mv maildropfilter.7 maildropfilter.7.in

maildropgdbm.html: maildropgdbm.sgml ../docbook/sgml2html
	../docbook/sgml2html maildropgdbm.sgml maildropgdbm.html

maildropgdbm.7: maildropgdbm.sgml ../docbook/sgml2html
	../docbook/sgml2man maildropgdbm.sgml maildropgdbm.7

maildropex.html: maildropex.sgml ../docbook/sgml2html
	../docbook/sgml2html maildropex.sgml maildropex.html

maildropex.7: maildropex.sgml ../docbook/sgml2html
	../docbook/sgml2man maildropex.sgml maildropex.7

mailbot.html: mailbot.sgml ../docbook/sgml2html
	../docbook/sgml2html mailbot.sgml mailbot.html

mailbot.1: mailbot.sgml ../docbook/sgml2html
	../docbook/sgml2man mailbot.sgml mailbot.1

reformail.html: reformail.sgml ../docbook/sgml2html
	../docbook/sgml2html reformail.sgml reformail.html

reformail.1: reformail.sgml ../docbook/sgml2html
	../docbook/sgml2man reformail.sgml reformail.1

makedat.html: makedat.sgml ../docbook/sgml2html
	../docbook/sgml2html makedat.sgml makedat.html

makedat.1: makedat.sgml ../docbook/sgml2html
	../docbook/sgml2man makedat.sgml makedat.1

endif

maildrop.html: maildrop.html.in
	./config.status --file=$@

maildrop.1: maildrop.1.in
	./config.status --file=$@

maildropfilter.html: maildropfilter.html.in
	./config.status --file=$@

maildropfilter.7: maildropfilter.7.in
	./config.status --file=$@

