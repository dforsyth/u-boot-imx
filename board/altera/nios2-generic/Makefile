#
# (C) Copyright 2001-2006
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
# (C) Copyright 2010, Thomas Chou <thomas@wytron.com.tw>
#
# SPDX-License-Identifier:	GPL-2.0+
#

ifneq ($(OBJTREE),$(SRCTREE))
$(shell mkdir -p $(obj)../common)
endif

obj-y	:= nios2-generic.o
obj-$(CONFIG_CMD_IDE) += ../common/cfide.o
obj-$(CONFIG_EPLED) += ../common/epled.o
obj-$(CONFIG_SEVENSEG) += ../common/sevenseg.o
obj-y	+= text_base.o
