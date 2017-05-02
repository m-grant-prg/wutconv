#! /usr/bin/env bash
#########################################################################
#									#
# Script ID: source/man/man1/Makefile.am				#
# Author: Mark Grant							#
#									#
# Purpose:								#
# AutoMake script file to generate wutconv manual pages from source.	#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 04/09/2014	MG	1.0.1	First release.				#
# 23/10/2015	MG	1.0.2	Restructure to conform to AutoTools	#
#				General Template v1.0.6.		#
# 02/05/2017	MG	1.0.3	Output from $(edit) was being ignored.	#
#									#
#########################################################################


wutconv.1: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).txt > $@.tmp
	txt2manwrap $(@F) 1 "Windows / Unix Text File Converter" $@.tmp $@
	rm -f $@.tmp

wutconv.1: $(srcdir)/wutconv.1.txt

man_MANS = wutconv.1

EXTRA_DIST = $(srcdir)/wutconv.1.txt

CLEANFILES = *.tmp wutconv.1
