#########################################################################
#									#
# Script ID: src/man/1/Makefile.am					#
# Author: Copyright (C) 2014-2019  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0					#
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
#				Rename source file extension .man.in	#
# 02/12/2017	MG	1.0.4	Determine the manual section from the	#
#				target suffix. If the suffix is blank	#
#				(foo.) or if there is no suffix (foo)	#
#				then error out.				#
#				Add SPDX license tags to source files.	#
# 10/02/2018	MG	1.0.5	Change file's header for new directory	#
#				names.					#
# 12/08/2019	MG	1.0.6	Remove shebang.				#
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
