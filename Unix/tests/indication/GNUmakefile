TOP = ../..
include $(TOP)/config.mak

CXXUNITTEST = test_indication

SOURCES = $(TOP)/ut/omitestcommon.cpp $(TOP)/ut/omifaultsimtest.cpp util.cpp \
	test_filter.cpp \
	test_listener.cpp \
	test_mgr.cpp \
	test_subscrip.cpp \
	test_classlist.cpp \
	test_e2e.cpp \

INCLUDES = $(TOP) $(TOP)/common

DEFINES = TEST_BUILD

LIBRARIES = test_util indimgr indicmn disp provmgr provreg miapi omi_error wsman http protocol sock xmlserializer wql xml base $(UNITTESTLIBS) micodec mofparser

include $(TOP)/mak/rules.mak

tests:
	$(call RUNUNITTEST)

##==============================================================================
##
## dep -- rule to build dependent libraries.
##
##==============================================================================
dep:
	( cd ../util; $(MAKE); )

reset:
	$(BINDIR)/nits -reset
