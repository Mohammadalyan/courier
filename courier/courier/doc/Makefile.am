#
# Copyright 1998 - 2009 Double Precision, Inc.  See COPYING for
# distribution information.


htmldocdir=@datadir@/htmldoc

CLEANFILES=permissions.dat

miscfiles=japanese_flag.png chinese_flag.png bg.gif icon.gif manpage.css \
		draft-varshavchik-exdata-smtpext.txt \
		draft-varshavchik-verp-smtpext.txt \
		draft-varshavchik-security-smtpext.txt \
		style.css frame.js

nohtmlinfiles=  aliases.html \
		changelog.html \
		courierd.html \
		courierdsn.html \
		documentation.html \
		esmtp.html \
		FAQ.html \
		footer.html \
		header.html \
		index.html \
		index2.html \
		install.html \
		intro.html \
		layout.html \
		links.html \
		local.html \
		main.html \
		menu.html \
		modules.html \
		queue.html \
		rpm.html \
		status.html \
		structures.html \
		svn.html

nohtmlin=$(miscfiles) $(nohtmlinfiles)

htmlin=\
		aliaslookup.html \
		cancelmsg.html \
		courier.html \
		courierldapaliasd.html \
		couriermlm.html \
		courierpop3d.html \
		couriertcpd.html \
		couriertls.html \
		deliverquota.html \
		dot-courier.html \
		dot-forward.html \
		esmtpd.html \
		imapd.html \
		localmailfilter.html \
		lockmail.html \
		mailbot.html \
		maildiracl.html \
		maildir.html \
		maildirkw.html \
		maildirmake.html \
		maildirquota.html \
		maildropex.html \
		maildropfilter.html \
		maildropgdbm.html \
		maildrop.html \
		maildrop.README.html \
		maildroptips.html \
		mailq.html \
		makeacceptmailfor.html \
		makealiases.html \
		makedat.html \
		makehosteddomains.html \
		makemime.html \
		makepercentrelay.html \
		makesmtpaccess.html \
		mimegpg.html \
		mkesmtpdcert.html \
		mkimapdcert.html \
		mkpop3dcert.html \
		pcp_README.html \
		pop3d.html \
		preline.html \
		reformail.html \
		reformime.html \
		sendmail.html \
		submit.html \
		testmxlookup.html \
		webmlmd.html


htmldoc_DATA=	$(nohtmlin) $(htmlin)

couriertcpd.html: ../../tcpd/couriertcpd.html
	cp -f $(srcdir)/../../tcpd/couriertcpd.html .

couriertcpd.1: ../../tcpd/couriertcpd.1
	cp -f $(srcdir)/../../tcpd/couriertcpd.1 .

couriertls.html: ../../tcpd/couriertls.html
	cp -f $(srcdir)/../../tcpd/couriertls.html .

couriertls.1: ../../tcpd/couriertls.1
	cp -f $(srcdir)/../../tcpd/couriertls.1 .

maildirmake.html: ../../maildir/maildirmake.html
	cp -f ../../maildir/maildirmake.html .

maildiracl.html: ../../maildir/maildiracl.html
	cp -f ../../maildir/maildiracl.html .

maildirkw.html: ../../maildir/maildirkw.html
	cp -f $(srcdir)/../../maildir/maildirkw.html .

maildirmake.1: ../../maildir/maildirmake.1
	cp -f ../../maildir/maildirmake.1 .

maildiracl.1: ../../maildir/maildiracl.1
	cp -f ../../maildir/maildiracl.1 .

maildirkw.1: ../../maildir/maildirkw.1
	cp -f $(srcdir)/../../maildir/maildirkw.1 .

maildir.html: ../../maildir/maildir.html
	cp -f $(srcdir)/../../maildir/maildir.html .

maildir.5: ../../maildir/maildir.5
	cp -f $(srcdir)/../../maildir/maildir.5 .

maildirquota.html: $(srcdir)/../../maildir/maildirquota.html
	cp -f $(srcdir)/../../maildir/maildirquota.html .

maildirquota.7: $(srcdir)/../../maildir/maildirquota.7
	cp -f $(srcdir)/../../maildir/maildirquota.7 .

deliverquota.html: ../../maildir/deliverquota.html
	cp -f ../../maildir/deliverquota.html .

deliverquota.8: ../../maildir/deliverquota.8
	cp -f ../../maildir/deliverquota.8 .

imapd.html: ../../imap/imapd.html
	cp -f ../../imap/imapd.html .

imapd.8: ../../imap/imapd.8
	cp -f ../../imap/imapd.8 .

maildrop.README.html: ../../maildrop/README.html
	cp -f ../../maildrop/README.html maildrop.README.html

lockmail.html: ../../liblock/lockmail.html
	cp -f $(srcdir)/../../liblock/lockmail.html .

lockmail.1: ../../liblock/lockmail.1
	cp -f $(srcdir)/../../liblock/lockmail.1 .

maildrop.html: ../../maildrop/maildrop.html
	cp -f ../../maildrop/maildrop.html .

maildrop.1: ../../maildrop/maildrop.1
	cp -f ../../maildrop/maildrop.1 .

maildropgdbm.html: ../../maildrop/maildropgdbm.html
	cp -f $(srcdir)/../../maildrop/maildropgdbm.html .

maildropgdbm.7: ../../maildrop/maildropgdbm.7
	cp -f $(srcdir)/../../maildrop/maildropgdbm.7 .

maildropex.html: ../../maildrop/maildropex.html
	cp -f $(srcdir)/../../maildrop/maildropex.html .

maildropex.7: ../../maildrop/maildropex.7
	cp -f $(srcdir)/../../maildrop/maildropex.7 .

maildroptips.html: ../../maildrop/maildroptips.html
	cp -f $(srcdir)/../../maildrop/maildroptips.html .

makedat.html: ../../maildrop/makedat.html
	cp -f $(srcdir)/../../maildrop/makedat.html .

makedat.1: ../../maildrop/makedat.1
	cp -f $(srcdir)/../../maildrop/makedat.1 .

maildropfilter.html: ../../maildrop/maildropfilter.html
	cp -f ../../maildrop/maildropfilter.html .

maildropfilter.7: ../../maildrop/maildropfilter.7
	cp -f ../../maildrop/maildropfilter.7 .

reformail.html: ../../maildrop/reformail.html
	cp -f $(srcdir)/../../maildrop/reformail.html .

reformail.1: ../../maildrop/reformail.1
	cp -f $(srcdir)/../../maildrop/reformail.1 .

makemime.html: ../../rfc2045/makemime.html
	cp -f $(srcdir)/../../rfc2045/makemime.html .

makemime.1: ../../rfc2045/makemime.1
	cp -f $(srcdir)/../../rfc2045/makemime.1 .

mailbot.html: ../../maildrop/mailbot.html
	cp -f $(srcdir)/../../maildrop/mailbot.html .

mailbot.1: ../../maildrop/mailbot.1
	cp -f $(srcdir)/../../maildrop/mailbot.1 .

reformime.html: ../../rfc2045/reformime.html
	cp -f $(srcdir)/../../rfc2045/reformime.html .

reformime.1: ../../rfc2045/reformime.1
	cp -f $(srcdir)/../../rfc2045/reformime.1 .

mimegpg.html: ../../gpglib/mimegpg.html
	cp -f $(srcdir)/../../gpglib/mimegpg.html mimegpg.html

mimegpg.1: ../../gpglib/mimegpg.html
	cp -f $(srcdir)/../../gpglib/mimegpg.1 mimegpg.1

mkimapdcert.html: ../../imap/mkimapdcert.html
	cp -f ../../imap/mkimapdcert.html .

mkimapdcert.8: ../../imap/mkimapdcert.8
	cp -f ../../imap/mkimapdcert.8 .

mkpop3dcert.html: ../../imap/mkpop3dcert.html
	cp -f ../../imap/mkpop3dcert.html .

mkpop3dcert.8: ../../imap/mkpop3dcert.8
	cp -f ../../imap/mkpop3dcert.8 .

courierpop3d.html: ../../imap/courierpop3d.html
	cp -f ../../imap/courierpop3d.html .

courierpop3d.8: ../../imap/courierpop3d.8
	cp -f ../../imap/courierpop3d.8 .

man1=sendmail.1 preline.1 maildirmake.1 cancelmsg.1 lockmail.1 maildrop.1 \
	mailq.1 mailbot.1 makemime.1 mimegpg.1 maildiracl.1 \
	makedat.1 reformail.1 reformime.1 couriermlm.1 testmxlookup.1 \
	dot-forward.1 couriertls.1 couriertcpd.1 maildirkw.1 \
	webmlmd.1

man5=dot-courier.5 maildir.5
man7=localmailfilter.7 maildirquota.7 maildropgdbm.7 maildropfilter.7 \
	maildropex.7
man8=aliaslookup.8 courier.8 courierldapaliasd.8 courierpop3d.8 \
	deliverquota.8 \
	esmtpd.8 makeacceptmailfor.8 makehosteddomains.8\
	mkesmtpdcert.8 mkimapdcert.8 mkpop3dcert.8 \
	makealiases.8 makepercentrelay.8 makesmtpaccess.8 \
	pop3d.8 pop3d-ssl.8 submit.8 imapd.8

pcp_README.html: ../../pcp/README.html
	cp -f $(srcdir)/../../pcp/README.html pcp_README.html


BUILT_SOURCES= \
	aliaslookup.html aliaslookup.8 \
	cancelmsg.html cancelmsg.1 \
	courier.html.in courier.8.in \
	courierldapaliasd.html.in courierldapaliasd.8.in \
	couriermlm.html.in couriermlm.1.in \
	dot-courier.html.in dot-courier.5.in \
	dot-forward.html dot-forward.1 \
	esmtpd.html.in esmtpd.8.in \
	localmailfilter.html.in localmailfilter.7.in \
	mailq.html mailq.1 \
	makeacceptmailfor.html.in makeacceptmailfor.8.in \
	makealiases.html.in makealiases.8.in \
	makehosteddomains.html.in makehosteddomains.8.in \
	makepercentrelay.html.in makepercentrelay.8.in \
	makesmtpaccess.html.in makesmtpaccess.8.in \
	mkesmtpdcert.html.in mkesmtpdcert.8.in \
	pop3d.html.in pop3d.8.in \
	preline.html.in preline.1.in \
	sendmail.html sendmail.1 \
	submit.html.in submit.8.in \
	testmxlookup.html testmxlookup.1 \
	webmlmd.html.in webmlmd.1.in

EXTRA_DIST=$(nohtmlin) $(BUILT_SOURCES) dotforward.1 pop3d-ssl.8

if HAVE_SGML

aliaslookup.html: aliaslookup.sgml ../../docbook/sgml2html
	../../docbook/sgml2html aliaslookup.sgml aliaslookup.html

aliaslookup.8: aliaslookup.sgml ../../docbook/sgml2man
	../../docbook/sgml2man aliaslookup.sgml aliaslookup.8


courier.html.in: courier.sgml ../../docbook/sgml2html
	../../docbook/sgml2html courier.sgml courier.html.in

courier.8.in: courier.sgml ../../docbook/sgml2man
	../../docbook/sgml2man courier.sgml courier.8.in
	mv courier.8 courier.8.in

cancelmsg.html: cancelmsg.sgml ../../docbook/sgml2html
	../../docbook/sgml2html cancelmsg.sgml cancelmsg.html

cancelmsg.1: cancelmsg.sgml ../../docbook/sgml2man
	../../docbook/sgml2man cancelmsg.sgml cancelmsg.1

mailq.html: mailq.sgml ../../docbook/sgml2html
	../../docbook/sgml2html mailq.sgml mailq.html

mailq.1: mailq.sgml ../../docbook/sgml2man
	../../docbook/sgml2man mailq.sgml mailq.1

couriermlm.html.in: couriermlm.sgml ../../docbook/sgml2html
	../../docbook/sgml2html couriermlm.sgml couriermlm.html.in

couriermlm.1.in: couriermlm.sgml ../../docbook/sgml2man
	../../docbook/sgml2man couriermlm.sgml couriermlm.1.in
	mv couriermlm.1 couriermlm.1.in

webmlmd.html.in: webmlmd.sgml ../../docbook/sgml2html
	../../docbook/sgml2html webmlmd.sgml webmlmd.html.in

webmlmd.1.in: webmlmd.sgml ../../docbook/sgml2man
	../../docbook/sgml2man webmlmd.sgml webmlmd.1.in
	mv webmlmd.1 webmlmd.1.in

dot-courier.html.in: dot-courier.sgml ../../docbook/sgml2html
	../../docbook/sgml2html dot-courier.sgml dot-courier.html.in

dot-courier.5.in: dot-courier.sgml ../../docbook/sgml2man
	../../docbook/sgml2man dot-courier.sgml dot-courier.5.in
	mv dot-courier.5 dot-courier.5.in

courierldapaliasd.html.in: courierldapaliasd.sgml ../../docbook/sgml2html
	../../docbook/sgml2html courierldapaliasd.sgml courierldapaliasd.html.in

courierldapaliasd.8.in: courierldapaliasd.sgml ../../docbook/sgml2man
	../../docbook/sgml2man courierldapaliasd.sgml courierldapaliasd.8.in
	mv courierldapaliasd.8 courierldapaliasd.8.in

esmtpd.html.in: esmtpd.sgml ../../docbook/sgml2html
	../../docbook/sgml2html esmtpd.sgml esmtpd.html.in

esmtpd.8.in: esmtpd.sgml ../../docbook/sgml2man
	../../docbook/sgml2man esmtpd.sgml esmtpd.8.in
	mv esmtpd.8 esmtpd.8.in

localmailfilter.html.in: localmailfilter.sgml ../../docbook/sgml2html
	../../docbook/sgml2html localmailfilter.sgml localmailfilter.html.in

localmailfilter.7.in: localmailfilter.sgml ../../docbook/sgml2man
	../../docbook/sgml2man localmailfilter.sgml localmailfilter.7.in
	mv localmailfilter.7 localmailfilter.7.in

makeacceptmailfor.html.in: makeacceptmailfor.sgml ../../docbook/sgml2html
	../../docbook/sgml2html makeacceptmailfor.sgml makeacceptmailfor.html.in

makeacceptmailfor.8.in: makeacceptmailfor.sgml ../../docbook/sgml2man
	../../docbook/sgml2man makeacceptmailfor.sgml makeacceptmailfor.8.in
	mv makeacceptmailfor.8 makeacceptmailfor.8.in

makealiases.html.in: makealiases.sgml ../../docbook/sgml2html
	../../docbook/sgml2html makealiases.sgml makealiases.html.in

makealiases.8.in: makealiases.sgml ../../docbook/sgml2man
	../../docbook/sgml2man makealiases.sgml makealiases.8.in
	mv makealiases.8 makealiases.8.in

makehosteddomains.html.in: makehosteddomains.sgml ../../docbook/sgml2html
	../../docbook/sgml2html makehosteddomains.sgml makehosteddomains.html.in

makehosteddomains.8.in: makehosteddomains.sgml ../../docbook/sgml2man
	../../docbook/sgml2man makehosteddomains.sgml makehosteddomains.8.in
	mv makehosteddomains.8 makehosteddomains.8.in

submit.html.in: submit.sgml ../../docbook/sgml2html
	../../docbook/sgml2html submit.sgml submit.html.in

submit.8.in: submit.sgml ../../docbook/sgml2man
	../../docbook/sgml2man submit.sgml submit.8.in
	mv submit.8 submit.8.in

pop3d.html.in: pop3d.sgml ../../docbook/sgml2html
	../../docbook/sgml2html pop3d.sgml pop3d.html.in

pop3d.8.in: pop3d.sgml ../../docbook/sgml2man
	../../docbook/sgml2man pop3d.sgml pop3d.8.in
	mv pop3d.8 pop3d.8.in

mkesmtpdcert.html.in: mkesmtpdcert.sgml ../../docbook/sgml2html
	../../docbook/sgml2html mkesmtpdcert.sgml mkesmtpdcert.html.in

mkesmtpdcert.8.in: mkesmtpdcert.sgml ../../docbook/sgml2man
	../../docbook/sgml2man mkesmtpdcert.sgml mkesmtpdcert.8.in
	mv mkesmtpdcert.8 mkesmtpdcert.8.in

makesmtpaccess.html.in: makesmtpaccess.sgml ../../docbook/sgml2html
	../../docbook/sgml2html makesmtpaccess.sgml makesmtpaccess.html.in

makesmtpaccess.8.in: makesmtpaccess.sgml ../../docbook/sgml2man
	../../docbook/sgml2man makesmtpaccess.sgml makesmtpaccess.8.in
	mv makesmtpaccess.8 makesmtpaccess.8.in

makepercentrelay.html.in: makepercentrelay.sgml ../../docbook/sgml2html
	../../docbook/sgml2html makepercentrelay.sgml makepercentrelay.html.in

makepercentrelay.8.in: makepercentrelay.sgml ../../docbook/sgml2man
	../../docbook/sgml2man makepercentrelay.sgml makepercentrelay.8.in
	mv makepercentrelay.8 makepercentrelay.8.in

sendmail.html: sendmail.sgml ../../docbook/sgml2html
	../../docbook/sgml2html sendmail.sgml sendmail.html

sendmail.1: sendmail.sgml ../../docbook/sgml2man
	../../docbook/sgml2man sendmail.sgml sendmail.1

testmxlookup.html: testmxlookup.sgml ../../docbook/sgml2html
	../../docbook/sgml2html testmxlookup.sgml testmxlookup.html

testmxlookup.1: testmxlookup.sgml ../../docbook/sgml2man
	../../docbook/sgml2man testmxlookup.sgml testmxlookup.1

dot-forward.html: dot-forward.sgml ../../docbook/sgml2html
	../../docbook/sgml2html dot-forward.sgml dot-forward.html

dot-forward.1: dot-forward.sgml ../../docbook/sgml2man
	../../docbook/sgml2man dot-forward.sgml dot-forward.1

preline.html.in: preline.sgml ../../docbook/sgml2html
	../../docbook/sgml2html preline.sgml preline.html.in

preline.1.in: preline.sgml ../../docbook/sgml2man
	../../docbook/sgml2man preline.sgml preline.1.in
	mv preline.1 preline.1.in

manpage.css: ../../docbook/manpage.css
	cp -f ../../docbook/manpage.css .

endif

courier.html: courier.html.in
	./config.status --file=$@

courier.8: courier.8.in
	./config.status --file=$@

couriermlm.html: couriermlm.html.in
	./config.status --file=$@

couriermlm.1: couriermlm.1.in
	./config.status --file=$@

webmlmd.html: webmlmd.html.in
	./config.status --file=$@

webmlmd.1: webmlmd.1.in
	./config.status --file=$@

dot-courier.html: dot-courier.html.in
	./config.status --file=$@

dot-courier.5: dot-courier.5.in
	./config.status --file=$@

courierldapaliasd.html: courierldapaliasd.html.in
	./config.status --file=$@

courierldapaliasd.8: courierldapaliasd.8.in
	./config.status --file=$@

esmtpd.html: esmtpd.html.in
	./config.status --file=$@

esmtpd.8: esmtpd.8.in
	./config.status --file=$@

localmailfilter.html: localmailfilter.html.in
	./config.status --file=$@

localmailfilter.7: localmailfilter.7.in
	./config.status --file=$@

makeacceptmailfor.html: makeacceptmailfor.html.in
	./config.status --file=$@

makeacceptmailfor.8: makeacceptmailfor.8.in
	./config.status --file=$@

makealiases.html: makealiases.html.in
	./config.status --file=$@

makealiases.8: makealiases.8.in
	./config.status --file=$@

makehosteddomains.html: makehosteddomains.html.in
	./config.status --file=$@

makehosteddomains.8: makehosteddomains.8.in
	./config.status --file=$@

submit.html: submit.html.in
	./config.status --file=$@

submit.8: submit.8.in
	./config.status --file=$@

pop3d.html: pop3d.html.in
	./config.status --file=$@

pop3d.8: pop3d.8.in
	./config.status --file=$@

mkesmtpdcert.html: mkesmtpdcert.html.in
	./config.status --file=$@

mkesmtpdcert.8: mkesmtpdcert.8.in
	./config.status --file=$@

makesmtpaccess.html: makesmtpaccess.html.in
	./config.status --file=$@

makesmtpaccess.8: makesmtpaccess.8.in
	./config.status --file=$@

makepercentrelay.html: makepercentrelay.html.in
	./config.status --file=$@

makepercentrelay.8: makepercentrelay.8.in
	./config.status --file=$@

preline.html: preline.html.in
	./config.status --file=$@

preline.1: preline.1.in
	./config.status --file=$@

install-man-extra:
	cd $(DESTDIR)$(man8dir) ; \
		rm -f courierpop3login.8 makesmtpaccess-msa.8 esmtpd-msa.8; \
		$(LN_S) courierpop3d.8 courierpop3login.8; \
		$(LN_S) makesmtpaccess.8 makesmtpaccess-msa.8 ; \
		$(LN_S) esmtpd.8 esmtpd-msa.8
	cd $(DESTDIR)$(man1dir) ; rm -f rmail.1 dotforward.1 \
		; $(LN_S) sendmail.1 rmail.1 \
		; $(LN_S) dot-forward.1 dotforward.1

uninstall-local:
	rm -f $(DESTDIR)$(man8dir)/esmtpd-msa.8
	rm -f $(DESTDIR)$(man8dir)/makesmtpaccess-msa.8
	rm -f $(DESTDIR)$(man8dir)/courierpop3login.8
	rm -f $(DESTDIR)$(man1dir)/rmail.1
	rm -f $(DESTDIR)$(man1dir)/dotforward.1

man_LINKS=$(man8dir)/courierpop3login.8 \
	$(man1dir)/rmail.1 $(man1dir)/dotforward.1 \
	$(man8dir)/makesmtpaccess-msa.8 \
	$(man8dir)/esmtpd-msa.8

man1dir=@mandir@/man1
man5dir=@mandir@/man5
man7dir=@mandir@/man7
man8dir=@mandir@/man8

man_MANS=$(man1) $(man5) $(man7) $(man8)

clean-local:
	rm -rf cleanlist
	mkdir cleanlist
	for f in $(EXTRA_DIST) ; do echo timestamp >cleanlist/$$f ; done
	for f in $(man_MANS) $(htmldoc_DATA) ; do test -f cleanlist/$$f || rm -f $$f ; done
	rm -rf cleanlist

install-data-hook:
	$(MAKE) install-man
	$(MAKE) install-man-extra
	$(MAKE) install-htmldocDATA
	$(MAKE) do-man-install

do-man-install:
	for f in $(mandir) $(man1dir) $(man7dir) $(man8dir) ; do test -d $(DESTDIR)$$f && chmod 755 $(DESTDIR)$$f ; done ; exit 0
	for f in $(man1) ; do test -f $(DESTDIR)$(man1dir)/$$f && chmod 644 $(DESTDIR)$(man1dir)/$$f ; done ; exit 0
	for f in $(man5) ; do test -f $(DESTDIR)$(man5dir)/$$f && chmod 644 $(DESTDIR)$(man5dir)/$$f ; done ; exit 0
	for f in $(man7) ; do test -f $(DESTDIR)$(man7dir)/$$f && chmod 644 $(DESTDIR)$(man7dir)/$$f ; done ; exit 0
	for f in $(man8) ; do test -f $(DESTDIR)$(man8dir)/$$f && chmod 644 $(DESTDIR)$(man8dir)/$$f ; done ; exit 0
	test -w /etc || exit 0 ; for f in $(mandir) $(man1dir) $(man5dir) $(man7dir) $(man8dir) ; do test -d $(DESTDIR)$$f && chown bin $(DESTDIR)$$f && chgrp bin $(DESTDIR)$$f ; done ; exit 0
	test -w /etc || exit 0 ; for f in $(man1) ; do test -f $(DESTDIR)$(man1dir)/$$f && chown bin $(DESTDIR)$(man1dir)/$$f && chgrp bin $(DESTDIR)$(man1dir)/$$f ; done ; exit 0
	test -w /etc || exit 0 ; for f in $(man5) ; do test -f $(DESTDIR)$(man5dir)/$$f && chown bin $(DESTDIR)$(man5dir)/$$f && chgrp bin $(DESTDIR)$(man5dir)/$$f ; done ; exit 0
	test -w /etc || exit 0 ; for f in $(man7) ; do test -f $(DESTDIR)$(man7dir)/$$f && chown bin $(DESTDIR)$(man7dir)/$$f && chgrp bin $(DESTDIR)$(man7dir)/$$f ; done ; exit 0
	test -w /etc || exit 0 ; for f in $(man8) ; do test -f $(DESTDIR)$(man8dir)/$$f && chown bin $(DESTDIR)$(man8dir)/$$f && chgrp bin $(DESTDIR)$(man8dir)/$$f ; done ; exit 0
	for f in $(htmldoc_DATA) ; do chmod 444 $(DESTDIR)$(htmldocdir)/$$f ; done
	test -w /etc || exit 0; for f in $(htmldoc_DATA) ; do chown bin $(DESTDIR)$(htmldocdir)/$$f ; chgrp bin $(DESTDIR)$(htmldocdir)/$$f ; done

status.html: config.status

install-perms:
	@$(MAKE) install-perms-recursive
	@$(MAKE) install-perms-local

install-perms-recursive:
	@>permissions.dat
	@SUBDIRS="$(SUBDIRS)" ; for f in $$SUBDIRS ; do ( cd $$f && $(MAKE) $(AM_MAKEFLAGS) install-perms ) ; cat /dev/null >>$$f/permissions.dat ; cat $$f/permissions.dat >>permissions.dat ; done

install-perms-local:
	@echo @mandir@ 755 bin bin >>permissions.dat
	@echo $(man1dir) 755 bin bin >>permissions.dat
	@echo $(man5dir) 755 bin bin >>permissions.dat
	@echo $(man7dir) 755 bin bin >>permissions.dat
	@echo $(man8dir) 755 bin bin >>permissions.dat
	@for f in $(man1) ; do	\
	echo $(man1dir)/$$f 644 bin bin man >>permissions.dat ; done
	@for f in $(man5) ; do	\
	echo $(man5dir)/$$f 644 bin bin man >>permissions.dat ; done
	@for f in $(man7) ; do	\
	echo $(man7dir)/$$f 644 bin bin man >>permissions.dat ; done
	@for f in $(man8) ; do	\
	echo $(man8dir)/$$f 644 bin bin man >>permissions.dat ; done
	@for f in $(man_LINKS) ; do	\
	echo $$f 644 bin bin man >>permissions.dat ; done
	@echo $(htmldocdir) 755 bin bin >>permissions.dat
	@for f in $(htmldoc_DATA) ; do \
	echo $(htmldocdir)/$$f 444 bin bin doc >>permissions.dat ; done

htmldocfiles=$(nohtmlinfiles) $(htmlin) \
	../module.fax/courierfax.html \
	../filters/courierfilter.html \
	../filters/courierperlfilter.html \
	../module.uucp/courieruucp.html \
	../filters/dupfilter.html

dollar=$$
id=$(dollar)Id

WWW=$$HOME/www/www.courier-mta.org

htmldoc: $(htmldocfiles)
	for f in $(htmldocfiles); do test "$$f" = "footer.html" && continue; test "$$f" = "menu.html" && continue; test "$$f" = "header.html" && continue; test "$$f" = "index.html" && continue; test "$$f" = "main.html" && continue; b=`basename $$f`; d=$(WWW)/$$b; h=`test ! -f $$d || perl -ne ' print $$1 if /\\$(id):([^\\$$]*)\\$$/' <$$d`; echo $$f; xsltproc --nonet $(WWW)/xsl/courier.xsl $$f | perl -ne 's~\$(id):.*\$$~\$(id):'"$$h"'\$$~; print' >$$d; done
	for f in index.html main.html header.html footer.html menu.html; do  b=`basename $$f`; d=$(WWW)/$$b; h=`test ! -f $$d || perl -ne ' print $$1 if /\\$(id):([^\\$$]*)\\$$/' <$$d`; perl -ne 's~\$(id):.*\$$~\$(id):'"$$h"'\$$~; print' <$$f >$$d; done
	cp $(miscfiles) $(WWW)
