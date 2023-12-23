#########################################################################
#									#
# Author: Copyright (C) 2014-2019, 2021, 2023  Mark Grant		#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
# AutoMake script file to generate wutconv manual pages from source.	#
#									#
#########################################################################


wutconv.1: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	$(edit) $(srcdir)/$(@F).man.in > $@.tmp
	targfile=$(@F);	\
	if [[ $$targfile == *"."* ]]; then \
		if [[ $${targfile##*.} == "" ]]; then \
			echo "Source file suffix used as section but empty."; \
			exit 1; \
		else \
			section=$${targfile##*.}; \
		fi; \
	else \
		echo "Source file suffix used as section but no dot & empty."; \
		exit 1; \
	fi; \
	txt2manwrap $(@F) $$section "Windows / Unix Text File Converter" \
		$@.tmp $@
	rm -f $@.tmp

wutconv.1: $(srcdir)/wutconv.1.man.in

man_MANS = wutconv.1

EXTRA_DIST = $(srcdir)/wutconv.1.man.in

CLEANFILES = *.tmp wutconv.1
