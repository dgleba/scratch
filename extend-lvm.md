# Issue extending LVM disk volume size, Ubuntu 14

I got this error.

```
albe@pmdsdata3:~$ sudo pvcreate /dev/sda7
  Device /dev/sda7 not found (or ignored by filtering).
```

I read about this..

```
albe@pmdsdata3:~$ sudo partprobe
[sudo] password for albe:
Warning: Unable to open /dev/sr0 read-write (Read-only file system).  /dev/sr0 has been opened read-only.
Warning: Unable to open /dev/sr0 read-write (Read-only file system).  /dev/sr0 has been opened read-only.
Error: /dev/sr0: unrecognised disk label
```

Which allowed it to work.

```
albe@pmdsdata3:~$ sudo pvcreate /dev/sda7
  Physical volume "/dev/sda7" successfully created
albe@pmdsdata3:~$

```

2019-05-17

### ref.

https://www.dropbox.com/s/cug0i5s5omyv9z3/expand%2Clinux%2Cdisk%2Cknow%2Cworks%2Cfdisk%2Cparted%2Cubuntu%2Cresize.txt?dl=0

C:\n\Dropbox\csd\serve\vboxyard\vamp_206a__notes\notes\expand,linux,disk,know,works,fdisk,parted,ubuntu,resize.txt
