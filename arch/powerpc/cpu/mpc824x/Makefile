#
# (C) Copyright 2000-2006
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# SPDX-License-Identifier:	GPL-2.0+
#

ifneq ($(OBJTREE),$(SRCTREE))
$(shell mkdir -p $(obj)drivers/epic $(obj)drivers/i2c)
endif

extra-y	= start.o
obj-y	= traps.o cpu.o cpu_init.o interrupts.o speed.o \
	  drivers/epic/epic1.o drivers/i2c/i2c.o pci.o
obj-y += bedbug_603e.o

SRCS += $(obj)bedbug_603e.c
$(obj)bedbug_603e.c:
	ln -sf $(src)../mpc8260/bedbug_603e.c $(obj)bedbug_603e.c
