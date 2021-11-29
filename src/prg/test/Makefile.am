#########################################################################
#									#
# Script ID: src/prg/test/Makefile.am					#
# Author: Copyright (C) 2019, 2021  Mark Grant				#
#									#
# Released under the GPLv3 only.					#
# SPDX-License-Identifier: GPL-3.0-only					#
#									#
# Purpose:								#
#	AutoMake script file to generate wutconv test program.		#
#									#
#########################################################################

#########################################################################
#									#
# Changelog								#
#									#
# Date		Author	Version	Description				#
#									#
# 14/08/2019	MG	1.0.1	First release.				#
# 29/11/2021	MG	1.0.2	Tighten SPDX tag.			#
#									#
#########################################################################


Test01.txt Test01Answer.txt Test01verbose.txt Test01verboseAnswer.txt \
Test02.txt Test02Answer.txt Test02verbose.txt Test02verboseAnswer.txt \
Test03.txt Test03Answer.txt Test03verbose.txt Test03verboseAnswer.txt \
Test04.txt Test04Answer.txt Test04verbose.txt Test04verboseAnswer.txt \
Test05File1.txt Test05File1Answer.txt Test05File2.txt Test05File2Answer.txt \
Test05File1verbose.txt Test05File1verboseAnswer.txt \
Test05File2verbose.txt Test05File2verboseAnswer.txt \
Test06File1.txt Test06File1Answer.txt Test06File2.txt Test06File2Answer.txt \
Test06File1verbose.txt Test06File1verboseAnswer.txt \
Test06File2verbose.txt Test06File2verboseAnswer.txt: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	cp $${srcdir}$(@F).in  $@
Test01.txt: $(srcdir)/Test01.txt.in
Test01Answer.txt: $(srcdir)/Test01Answer.txt.in
Test01verbose.txt: $(srcdir)/Test01verbose.txt.in
Test01verboseAnswer.txt: $(srcdir)/Test01verboseAnswer.txt.in
Test02.txt: $(srcdir)/Test02.txt.in
Test02Answer.txt: $(srcdir)/Test02Answer.txt.in
Test02verbose.txt: $(srcdir)/Test02verbose.txt.in
Test02verboseAnswer.txt: $(srcdir)/Test02verboseAnswer.txt.in
Test03.txt: $(srcdir)/Test03.txt.in
Test03Answer.txt: $(srcdir)/Test03Answer.txt.in
Test03verbose.txt: $(srcdir)/Test03verbose.txt.in
Test03verboseAnswer.txt: $(srcdir)/Test03verboseAnswer.txt.in
Test04.txt: $(srcdir)/Test04.txt.in
Test04Answer.txt: $(srcdir)/Test04Answer.txt.in
Test04verbose.txt: $(srcdir)/Test04verbose.txt.in
Test04verboseAnswer.txt: $(srcdir)/Test04verboseAnswer.txt.in
Test05File1.txt: $(srcdir)/Test05File1.txt.in
Test05File1Answer.txt: $(srcdir)/Test05File1Answer.txt.in
Test05File2.txt: $(srcdir)/Test05File2.txt.in
Test05File2Answer.txt: $(srcdir)/Test05File2Answer.txt.in
Test05File1verbose.txt: $(srcdir)/Test05File1verbose.txt.in
Test05File1verboseAnswer.txt: $(srcdir)/Test05File1verboseAnswer.txt.in
Test05File2verbose.txt: $(srcdir)/Test05File2verbose.txt.in
Test05File2verboseAnswer.txt: $(srcdir)/Test05File2verboseAnswer.txt.in
Test06File1.txt: $(srcdir)/Test06File1.txt.in
Test06File1Answer.txt: $(srcdir)/Test06File1Answer.txt.in
Test06File2.txt: $(srcdir)/Test06File2.txt.in
Test06File2Answer.txt: $(srcdir)/Test06File2Answer.txt.in
Test06File1verbose.txt: $(srcdir)/Test06File1verbose.txt.in
Test06File1verboseAnswer.txt: $(srcdir)/Test06File1verboseAnswer.txt.in
Test06File2verbose.txt: $(srcdir)/Test06File2verbose.txt.in
Test06File2verboseAnswer.txt: $(srcdir)/Test06File2verboseAnswer.txt.in


check_DATA = Test01.txt Test01Answer.txt Test01verbose.txt \
	Test01verboseAnswer.txt \
	Test02.txt Test02Answer.txt Test02verbose.txt \
	Test02verboseAnswer.txt \
	Test03.txt Test03Answer.txt Test03verbose.txt \
	Test03verboseAnswer.txt \
	Test04.txt Test04Answer.txt Test04verbose.txt \
	Test04verboseAnswer.txt \
	Test05File1.txt Test05File1Answer.txt Test05File2.txt \
	Test05File2Answer.txt Test05File1verbose.txt \
	Test05File1verboseAnswer.txt Test05File2verbose.txt \
	Test05File2verboseAnswer.txt \
	Test06File1.txt Test06File1Answer.txt Test06File2.txt \
	Test06File2Answer.txt Test06File1verbose.txt \
	Test06File1verboseAnswer.txt Test06File2verbose.txt \
	Test06File2verboseAnswer.txt


test01.sh test01verbose.sh test02.sh test02verbose.sh \
test03.sh test03verbose.sh test04.sh test04verbose.sh \
test05.sh test05verbose.sh test06.sh test06verbose.sh test-menu.sh: Makefile
	mkdir -p $(@D)
	rm -f $@ $@.tmp
	test -f ./$@.in || srcdir=$(srcdir)/; \
	$(edit) $${srcdir}$(@F).in > $@.tmp
	mv $@.tmp $@
	chmod a+x $@
test01.sh: $(srcdir)/test01.sh.in
test01verbose.sh: $(srcdir)/test01verbose.sh.in
test02.sh: $(srcdir)/test02.sh.in
test02verbose.sh: $(srcdir)/test02verbose.sh.in
test03.sh: $(srcdir)/test03.sh.in
test03verbose.sh: $(srcdir)/test03verbose.sh.in
test04.sh: $(srcdir)/test04.sh.in
test04verbose.sh: $(srcdir)/test04verbose.sh.in
test05.sh: $(srcdir)/test05.sh.in
test05verbose.sh: $(srcdir)/test05verbose.sh.in
test06.sh: $(srcdir)/test06.sh.in
test06verbose.sh: $(srcdir)/test06verbose.sh.in
test-menu.sh: $(srcdir)/test-menu.sh.in

check_SCRIPTS = test01.sh test01verbose.sh \
	test02.sh test02verbose.sh \
	test03.sh test03verbose.sh \
	test04.sh test04verbose.sh \
	test05.sh test05verbose.sh \
	test06.sh test06verbose.sh \
	test-menu.sh

EXTRA_DIST = $(srcdir)/Test01.txt.in $(srcdir)/Test01Answer.txt.in \
	$(srcdir)/Test01verbose.txt.in $(srcdir)/Test01verboseAnswer.txt.in \
	$(srcdir)/test01.sh.in $(srcdir)/test01verbose.sh.in \
	$(srcdir)/Test02.txt.in $(srcdir)/Test02Answer.txt.in \
	$(srcdir)/Test02verbose.txt.in $(srcdir)/Test02verboseAnswer.txt.in \
	$(srcdir)/test02.sh.in $(srcdir)/test02verbose.sh.in \
	$(srcdir)/Test03.txt.in $(srcdir)/Test03Answer.txt.in \
	$(srcdir)/Test03verbose.txt.in $(srcdir)/Test03verboseAnswer.txt.in \
	$(srcdir)/test03.sh.in $(srcdir)/test03verbose.sh.in \
	$(srcdir)/Test04.txt.in $(srcdir)/Test04Answer.txt.in \
	$(srcdir)/Test04verbose.txt.in $(srcdir)/Test04verboseAnswer.txt.in \
	$(srcdir)/test04.sh.in $(srcdir)/test04verbose.sh.in \
	$(srcdir)/Test05File1.txt.in $(srcdir)/Test05File1Answer.txt.in \
	$(srcdir)/Test05File2.txt.in $(srcdir)/Test05File2Answer.txt.in \
	$(srcdir)/Test05File1verbose.txt.in \
	$(srcdir)/Test05File1verboseAnswer.txt.in \
	$(srcdir)/Test05File2verbose.txt.in \
	$(srcdir)/Test05File2verboseAnswer.txt.in \
	$(srcdir)/test05.sh.in $(srcdir)/test05verbose.sh.in \
	$(srcdir)/Test06File1.txt.in $(srcdir)/Test06File1Answer.txt.in \
	$(srcdir)/Test06File2.txt.in $(srcdir)/Test06File2Answer.txt.in \
	$(srcdir)/Test06File1verbose.txt.in \
	$(srcdir)/Test06File1verboseAnswer.txt.in \
	$(srcdir)/Test06File2verbose.txt.in \
	$(srcdir)/Test06File2verboseAnswer.txt.in \
	$(srcdir)/test06.sh.in $(srcdir)/test06verbose.sh.in \
	$(srcdir)/test-menu.sh.in


TESTS = test01.sh test01verbose.sh
TESTS += test02.sh test02verbose.sh
TESTS += test03.sh test03verbose.sh
TESTS += test04.sh test04verbose.sh
TESTS += test05.sh test05verbose.sh
TESTS += test06.sh test06verbose.sh


CLEANFILES = *.tmp *.sh *.txt

