ifneq ($(KERNELRELEASE),)
	obj-m:= ledDriverModule.o
	ledDriverModule-objs:= ledDriver.o
else
	KERNELDIR ?= /root/pxadev/kernel/linux-2.6.12.4-col2/
	PWD := $(shell pwd)

.phony: all
all:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) modules

phony: clean
clean:
	rm -f *.o *.mod.c *.ko

endif

