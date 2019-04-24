TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = ptest
# ptest.dbd will be created and installed
DBD += ptest.dbd

# ptest.dbd will be made up from these files:
ptest_DBD += base.dbd

# Include dbd files from all support applications:
ptest_DBD += ptools.dbd

# Add all the support libraries needed by this IOC
ptest_LIBS += ptools

# ptest_registerRecordDeviceDriver.cpp derives from ptest.dbd
ptest_SRCS += ptest_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
ptest_SRCS_DEFAULT += ptestMain.cpp
ptest_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#ptest_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
ptest_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

