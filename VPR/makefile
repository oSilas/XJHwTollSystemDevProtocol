# ----------------------------------------------------------------------
#
# This makefile has been automatically generated by WinGDB 3.7, build 2056
# Do not edit.
#
# Project: VPR
#
# ----------------------------------------------------------------------

PLATFORM=unix

ifneq ("$(windir)","")
PLATFORM=windows
endif

ifneq ("$(WinDir)","")
PLATFORM=windows
endif

ifneq ("$(WINDIR)","")
PLATFORM=windows
endif

UNAME=$(shell uname -o)

ifeq ("$(UNAME)","Cygwin")
PLATFORM=cygwin
endif

ifeq ("$(BUILD_CONFIGURATION)","")
	BUILD_CONFIGURATION=Debug
endif

ifeq ("$(BUILD_CONFIGURATION)","Debug")
CC= gcc
CXX= g++
AR= ar
CFLAGS= -g
CXXFLAGS= -g
ARFLAGS= cru
LDFLAGS= -lpthread -ldl -L /usr/lib/ -L ./ -g
RESULT=VPR
INTERMEDIATE_DIR=Debug/obj
DESTINATION_DIR=Debug/bin
ifeq ("$(PLATFORM)","cygwin")
	RM=rm -f
	MKDIR=mkdir -p
	INTERMEDIATE_DIR_MK=$(INTERMEDIATE_DIR)
	DESTINATION_DIR_MK=$(DESTINATION_DIR)
else
	RM= rm -f
	MKDIR= mkdir -p
	INTERMEDIATE_DIR_MK=Debug/obj
	DESTINATION_DIR_MK=Debug/bin
endif

endif

ifeq ("$(BUILD_CONFIGURATION)","Release")
CC= gcc
CXX= g++
AR= ar
CFLAGS= -g
CXXFLAGS= -g
ARFLAGS= cru
LDFLAGS= -g
RESULT=VPR
INTERMEDIATE_DIR=Debug/obj
DESTINATION_DIR=Debug/bin
ifeq ("$(PLATFORM)","cygwin")
	RM=rm -f
	MKDIR=mkdir -p
	INTERMEDIATE_DIR_MK=$(INTERMEDIATE_DIR)
	DESTINATION_DIR_MK=$(DESTINATION_DIR)
else
	RM= rm -f
	MKDIR= mkdir -p
	INTERMEDIATE_DIR_MK=Debug/obj
	DESTINATION_DIR_MK=Debug/bin
endif

endif

SOURCES= main.c pub.c vpr_sdk.c

SOURCEPATHS= main.c pub.c vpr_sdk.c

HEADERS= pub.h vpr_sdk.h

VPATH= $(INTERMEDIATE_DIR)

OBJECTNAMES=$(patsubst %.c,%.o,$(patsubst %.cpp,%.o,$(SOURCES)))
OBJECTPATHS=$(addprefix $(INTERMEDIATE_DIR)/,$(OBJECTNAMES))

$(DESTINATION_DIR)/$(RESULT): $(OBJECTNAMES)
ifeq ("$(wildcard $(DESTINATION_DIR) )","")
	-$(MKDIR) $(DESTINATION_DIR_MK)
endif
	$(CC) $(SYSROOTFLAGS) $(OBJECTPATHS) -o $@ $(LDFLAGS)

$(INTERMEDIATE_DIR)/VPR.d: $(SOURCES) $(HEADERS)
ifeq ("$(wildcard $(DESTINATION_DIR) )","")
	-$(MKDIR) $(DESTINATION_DIR_MK)
endif
ifeq ("$(wildcard $(INTERMEDIATE_DIR) )","")
	-$(MKDIR) $(INTERMEDIATE_DIR_MK)
endif
	$(CXX) $(CXXFLAGS) -MM $(SOURCEPATHS) > $@

-include $(INTERMEDIATE_DIR)/VPR.d

clean:
	$(RM) $(DESTINATION_DIR)/$(RESULT)
	$(RM) $(INTERMEDIATE_DIR)/VPR.d
	$(RM) $(OBJECTPATHS)

%.o: %.cpp
	$(CXX) $(CXXFLAGS) -c -o $(INTERMEDIATE_DIR)/$@ $<

%.o: %.c
	$(CC) $(CFLAGS) -c -o $(INTERMEDIATE_DIR)/$@ $<
