
AM_CPPFLAGS = -I${top_srcdir} -I${top_builddir}

if AUTO_EXAMPLES
bin_PROGRAMS = MultidimIntegral
TESTS = MultidimIntegral$(EXEEXT)
else
noinst_PROGRAMS = MultidimIntegral
endif
MultidimIntegral_SOURCES = MultidimIntegral.cpp
MultidimIntegral_LDADD = ../../ql/libQuantLib.la ${BOOST_THREAD_LIB}

EXTRA_DIST = \
    CMakeLists.txt \
    MultidimIntegral_vc9.vcproj \
    MultidimIntegral.vcxproj \
    MultidimIntegral.vcxproj.filters

.PHONY: examples check-examples

examples: MultidimIntegral$(EXEEXT)

check-examples: examples
	./MultidimIntegral$(EXEEXT)

dist-hook:
	mkdir -p $(distdir)/bin
	mkdir -p $(distdir)/build

