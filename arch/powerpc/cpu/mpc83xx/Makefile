#
# (C) Copyright 2006
# Wolfgang Denk, DENX Software Engineering, wd@denx.de.
#
# Copyright 2004 Freescale Semiconductor, Inc.
#
# SPDX-License-Identifier:	GPL-2.0+
#

MINIMAL=

ifdef CONFIG_SPL_BUILD
ifdef CONFIG_SPL_INIT_MINIMAL
MINIMAL=y
endif
endif

extra-y	= start.o

ifdef MINIMAL

obj-y	+= spl_minimal.o

else

obj-y += traps.o
obj-y += cpu.o
obj-y += cpu_init.o
obj-y += speed.o
obj-y += interrupts.o
obj-y += ecc.o
obj-$(CONFIG_QE) += qe_io.o
obj-$(CONFIG_FSL_SERDES) += serdes.o
obj-$(CONFIG_PCI) += pci.o
obj-$(CONFIG_PCIE) += pcie.o
obj-$(CONFIG_OF_LIBFDT) += fdt.o

# Stub implementations of cache management functions for USB
obj-y += cache.o

ifdef CONFIG_FSL_DDR2
obj-$(CONFIG_MPC8349) += ddr-gen2.o
SRCS += $(obj)ddr-gen2.c
else
obj-y += spd_sdram.o
endif
obj-$(CONFIG_FSL_DDR2) += law.o

endif # not minimal

$(obj)ddr-gen1.c:
	ln -sf $(SRCTREE)/arch/powerpc/cpu/mpc85xx/ddr-gen1.c $(obj)ddr-gen1.c

$(obj)ddr-gen2.c:
	ln -sf $(SRCTREE)/arch/powerpc/cpu/mpc85xx/ddr-gen2.c $(obj)ddr-gen2.c

$(obj)ddr-gen3.c:
	ln -sf $(SRCTREE)/arch/powerpc/cpu/mpc85xx/ddr-gen3.c $(obj)ddr-gen3.c
