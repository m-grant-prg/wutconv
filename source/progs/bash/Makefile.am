#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: source/progs/bash/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## AutoMake script file to generate wutconv script from source.		##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 04/09/2014	MG	1.0.1	First release.				##
## 29/11/2014	MG	1.0.2	Add script substitution variable for	##
##				overall package version.		##
## 23/10/2015	MG	1.0.3	Restructure to conform to AutoTools	##
##				General Template v1.0.6.		##
##									##
##########################################################################


wutconv: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
wutconv: $(srcdir)/wutconv.in

bin_SCRIPTS = wutconv

EXTRA_DIST = $(srcdir)/wutconv.in

CLEANFILES = *.tmp wutconv

