CROSS_COMPILE?=aarch64-linux-gnu-
INCLUDE_PATH:=/mnt/nfs_server/linux/5.15.84/include/
KERNEL_SOURCES_PATH:=/mnt/nfs_server/linux/5.15.84/

obj-m+=rpichar.o

all:
	make ARCH=arm64 CROSS_COMPILE=$(CROSS_COMPILE) -I $(INCLUDE_PATH) -C $(KERNEL_SOURCES_PATH) M=$(PWD) modules
	$(CROSS_COMPILE)gcc testrpichar.c -I $(INCLUDE_PATH) -o test
clean:
	make -I $(INCLUDE_PATH) -C $(KERNEL_SOURCES_PATH) M=$(PWD) clean
	rm test
