obj-m += usersync.o
EXTRA_CFLAGS=-std=gnu99
K=$(shell uname -r)
M=$(PWD)

all:
	make -C /lib/modules/$(K)/build M=$(M) modules
	gcc call_create.c -o call_create

inst:
	make -C /lib/modules/$(K)/build M=$(M) modules_install

clean:
	make -C /lib/modules/$(K)/build M=$(M) clean
	rm call_create
