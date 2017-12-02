#! /usr/bin/env bash
#########################################################################
#									#
# Script ID: source/progs/bash/Makefile.am				#
# Author: Copyright (C) 2014-2017  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0					#
#									#
# Purpose:								#
# AutoMake script file to generate wutconv script from source.		#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 04/09/2014	MG	1.0.1	First release.				#
# 29/11/2014	MG	1.0.2	Add script substitution variable for	#
#				overall package version.		#
# 23/10/2015	MG	1.0.3	Restructure to conform to AutoTools	#
#				General Template v1.0.6.		#
# 02/05/2017	MG	1.0.4	Rename source file extension .sh.in	#
# 02/12/2017	MG	1.0.5	Add SPDX license tags to source files.	#
#									#
#########################################################################


wutconv: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.sh.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).sh.in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
wutconv: $(srcdir)/wutconv.sh.in

bin_SCRIPTS = wutconv

EXTRA_DIST = $(srcdir)/wutconv.sh.in

CLEANFILES = *.tmp wutconv
