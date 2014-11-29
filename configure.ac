##########################################################################
##									##
## Script ID: ./configure.ac						##
## Author: Mark Grant							##
##									##
## Purpose:								##
## Autoconfigure script file to configure wutconv project.		##
##									##
##########################################################################

##########################################################################
##									##
## Changelog								##
##									##
## Date		Author	Version	Description				##
##									##
## 04/09/2014	MG	1.0.1	First release.				##
## 29/11/2014	MG	1.0.2	Remove redundant hashpling.		##
## 29/11/2014	MG	1.0.3	Add getopt processing to allowing for	##
##				FreeBSD quirk of 2 different getopt	##
##				programs on PATH. See comments in	##
##				script at the start of "Main". 		##
##				Structure OS specific requirements to	##
##				test for generic *BSD OSs and use	##
##				Linux as the default.			##
##									##
##########################################################################

AC_PREREQ([2.65])
AC_INIT([Windows / Unix File Converter], m4_esyscmd([git describe --always 1>/dev/null 2>/dev/null && git describe --always | tr -d '\n' || echo 'Pre-Release' | tr -d '\n']), [m.grant.prg@gmail.com], [wutconv])

AM_INIT_AUTOMAKE

AC_CONFIG_FILES([Makefile
		 src/scripts/Makefile
		 src/manpages/man1/Makefile])


AC_CANONICAL_HOST

# Checks for programs.
AC_MSG_NOTICE([checking for required $host_os specific programs])
case $host_os in
	*bsd*)	AC_MSG_NOTICE([using $host_os...])
		AC_CHECK_PROG(GETOPT, getopt, yes, no, path = '/usr/local/bin')
		if test "x$GETOPT" = "xno" ; then
			AC_MSG_ERROR([getopt not found])
		fi
		;;
	# linux*)	Allow fall through for now as the defaults are linux.
	*)	AC_MSG_NOTICE([using defaults...])
		AC_CHECK_PROG(GETOPT, getopt, yes, no)
		if test "x$GETOPT" = "xno" ; then
			AC_MSG_ERROR([getopt not found])
		fi
		;;
esac

AC_MSG_NOTICE([checking for required generic programs])
AC_CHECK_PROG(BASH, bash, yes, no)
if test "x$BASH" = "xno" ; then
   	AC_MSG_ERROR([bash not found])
fi

AC_CHECK_PROG(AWK, awk, yes, no)
if test "x$AWK" = "xno" ; then
   	AC_MSG_ERROR([awk not found])
fi

AC_CHECK_PROG(TXT2MAN, txt2man, yes, no)
if test "x$TXT2MAN" = "xno" ; then
   	AC_MSG_ERROR([txt2man not found])
fi

# Checks for libraries.

# Checks for header files.

# Checks for typedefs, structures, and compiler characteristics.

# Checks for library functions.

AC_OUTPUT
