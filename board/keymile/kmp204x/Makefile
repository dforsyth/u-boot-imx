#
# (C) Copyright 2001-2007
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# See file CREDITS for list of people who contributed to this
# project.
#
# SPDX-License-Identifier:	GPL-2.0+
#

ifneq ($(OBJTREE),$(SRCTREE))
$(shell mkdir -p $(obj)../common)
endif

obj-y	:= $(BOARD).o ddr.o eth.o tlb.o pci.o law.o \
	../common/common.o ../common/ivm.o
