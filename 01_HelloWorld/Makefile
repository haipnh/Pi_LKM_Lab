obj-m+=hello.o

all:
	make -I /mnt/nfs_server/linux/include/ -C /mnt/nfs_server/linux/ M=$(PWD) modules
clean:
	make -I /mnt/nfs_server/linux/include/ -C /mnt/nfs_server/linux/ M=$(PWD) clean