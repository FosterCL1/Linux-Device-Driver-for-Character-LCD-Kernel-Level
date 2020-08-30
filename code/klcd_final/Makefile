#
# 	A Makefile to cross-compile a kernel module
#
#	(from a Ubuntu PC to a Beaglebone Black ARM target board)
#

obj-m	:= klcd.o
 
KDIR    := /home/colin/src/beagleboneKernel/kernel/linux/
PWD	:= $(shell pwd) 
 
default:
	$(MAKE) ARCH:=arm CROSS_COMPILE:=/usr/bin/arm-linux-gnueabi- \
	-C $(KDIR) M=$(PWD) modules 

clean:	
	$(MAKE) -C $(KDIR) M=$(PWD) clean
	rm -rf *.ko
	rm -rf *.mod.*
	rm -rf .*.cmd
	rm -rf *.o
	rm -rf *.order
	rm -rf *.symvers
	rm -rf *.c~
	rm -rf *.h~
	
