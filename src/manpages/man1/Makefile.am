#! /usr/bin/env bash
##########################################################################
##									##
## Script ID: src/manpages/man1/Makefile.am				##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Automake script file to generate wutconv manual pages from source.	##
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


manpagessrcdir = $(srcdir)

../../../manpages/man1/wutconv.1: Makefile
	mkdir -p $(@D)
	rm -f $@
	txt2man -t wutconv -s 1 -v "Windows / Unix Text File Converter" \
		$(manpagessrcdir)/$(@F).txt > $@

wutconv.1: $(manpagessrcdir)/wutconv.1.txt

man1_MANS = ../../../manpages/man1/wutconv.1

EXTRA_DIST = $(manpagessrcdir)/wutconv.1.txt
