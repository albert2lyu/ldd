export ARCH=arm
export CROSS_COMPILE=arm-linux-gnueabihf-
export AS=${CROSS_COMPILE}as
KERNEL=$(HOME)/kernel

obj-m += main.o
main-objs:= ldd.o
all:
	$(AS) -o ldd.o ldd.S
	make -C $(KERNEL) M=$(PWD) modules

clean:
	make -C $(KERNEL) M=$(PWD) clean
