# apue
APUE third edition learning

0. souce website: http://www.apuebook.com

1. fix make error on centos7

error：
```shell
gcc -ansi -I../include -Wall -DLINUX -D_GNU_SOURCE  barrier.c -o barrier  -L../lib -lapue -pthread -lrt -lbsd
/tmp/cc0MBwPF.o: In function `thr_fn':
barrier.c:(.text+0x80): undefined reference to `heapsort'
collect2: error: ld returned 1 exit status
make[1]: *** [barrier] Error 1
make[1]: Leaving directory `/root/apue/apue.3e/threads'
make: *** [all] Error 1
```
fix:
```shell
yum install -y libbsd-devel
```
