#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/scripts/Makefile.am					##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate wutconv script from source.		##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 04/09/2014	MG	1.0.1	First release.				##
##									##
##########################################################################


edit = sed \
	-e 's|@bindir[@]|$(bindir)|g' \
	-e 's|@pkgdatadir[@]|$(pkgdatadir)|g' \
	-e 's|@sysconfdir[@]|$(sysconfdir)|g' \
	-e 's|@prefix[@]|$(prefix)|g' \
	-e 's|@DWNUTIL[@]|$(DWNUTIL)|g'

scriptssrcdir = $(srcdir)

../../scripts/wutconv: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || scriptssrcdir=$(scriptssrcdir)/; \
	$(edit) $${scriptssrcdir}$(@F).in >$@.tmp

	mv $@.tmp $@

	chmod a+x $@

wutconv: $(scriptssrcdir)/wutconv.in

bin_SCRIPTS = ../../scripts/wutconv

EXTRA_DIST = $(scriptssrcdir)/wutconv.in
