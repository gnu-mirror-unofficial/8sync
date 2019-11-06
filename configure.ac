AC_INIT([8sync], [0.4.2], [cwebber@dustycloud.org])

AC_CANONICAL_HOST

GUILE_PKG([3.0 2.2])
guilemoduledir="${datarootdir}/guile/site/$GUILE_EFFECTIVE_VERSION"
guileobjectdir="${libdir}/guile/$GUILE_EFFECTIVE_VERSION/site-ccache"
AC_SUBST([guilemoduledir])
AC_SUBST([guileobjectdir])

AM_INIT_AUTOMAKE([-Wall -Werror foreign])

m4_ifdef([GUILE_PROGS],
         [],
         [AC_ERROR(could not locate guile aclocal macros)])

GUILE_PROGS

AC_CONFIG_FILES([Makefile])
AC_CONFIG_FILES([env], [chmod +x env])
AC_CONFIG_FILES([pre-inst-env], [chmod +x pre-inst-env])
AC_OUTPUT
