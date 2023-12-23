#########################################################################
#									#
# Author: Copyright (C) 2014-2019, 2021, 2023  Mark Grant		#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate wutconv script from source.		#
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
