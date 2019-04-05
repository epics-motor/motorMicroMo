TOP=../..

include $(TOP)/configure/CONFIG
#----------------------------------------
#  ADD MACRO DEFINITIONS AFTER THIS LINE
#=============================

#=============================
# Build the IOC application

PROD_IOC = microMo
# microMo.dbd will be created and installed
DBD += microMo.dbd

# microMo.dbd will be made up from these files:
microMo_DBD += base.dbd

# Include dbd files from all support applications:
#microMo_DBD += xxx.dbd

# Add all the support libraries needed by this IOC
#microMo_LIBS += xxx

# microMo_registerRecordDeviceDriver.cpp derives from microMo.dbd
microMo_SRCS += microMo_registerRecordDeviceDriver.cpp

# Build the main IOC entry point on workstation OSs.
microMo_SRCS_DEFAULT += microMoMain.cpp
microMo_SRCS_vxWorks += -nil-

# Add support from base/src/vxWorks if needed
#microMo_OBJS_vxWorks += $(EPICS_BASE_BIN)/vxComLibrary

# Finally link to the EPICS Base libraries
microMo_LIBS += $(EPICS_BASE_IOC_LIBS)

#===========================

include $(TOP)/configure/RULES
#----------------------------------------
#  ADD RULES AFTER THIS LINE

