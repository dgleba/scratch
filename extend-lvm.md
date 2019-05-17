# Issue extending

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
