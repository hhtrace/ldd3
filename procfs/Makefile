ifneq ($(KERNELRELEASE),)
# call from kernel build system

obj-m	:= procfs_test1.o
obj-m	+= procfs_test2.o
obj-m	+= procfs_test3.o

else

KERNELDIR ?= /lib/modules/$(shell uname -r)/build
PWD       := $(shell pwd)

default:
	$(MAKE) -C $(KERNELDIR) M=$(PWD) LDDINCDIR=$(PWD)/../include modules

endif



clean:
	rm -rf *.o *~ core .depend .*.cmd *.ko *.mod.c .tmp_versions

