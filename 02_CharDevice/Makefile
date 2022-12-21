obj-m+=ebbchar.o

all:
	make -I /mnt/nfs_server/linux/include/ -C /mnt/nfs_server/linux/ M=$(PWD) modules
	$(CC) testebbchar.c -I /mnt/nfs_server/linux/include/ -o test
clean:
	make -I /mnt/nfs_server/linux/include/ -C /mnt/nfs_server/linux/ M=$(PWD) clean
	rm test