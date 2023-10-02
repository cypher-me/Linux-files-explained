# Linux File system
Source of this info is from [Youtube](https://www.youtube.com/watch?v=HbgzrKJvDRw&list=PPSV) <br>
Linux uses the file system hierachy standard <br>
maintained by the linux foundation.<br>
In linux everything is a file.


### /bin (binaries)

basic binaries/application eg ls, chmod and chown. <br>
Containes binaries that are needed in single user mode <br>

### /boot

Proceed with caution. <br>
Contains everything the os needs to boot.<br>
The location of the boot loader.

### /cdrom > not in all distros.

Leagcy mounting point for your cd rom.

### /dev (devices)

Hardware as files.<br>
Hardware files e.g the disk file is `/dev/sda` <br>
A partion in that disk is `/dev/sda1` or `/dev/sda2`<br>
This is accesed by drivers and applications not to be messed by users(unless you know what you are doing).

### /etc (et cetra)

This is where configurations are stored <br>
The configurations are for system wide applications.

### /home

Each user has its own directory <br>
Each user can only access there own. <br>
It can be mounted in a different drive or partition. <br> 
Which allows you to reinstall you system and preserve <br>
your files .
It also containes hidden files and directories which <br>
store application settings. 



### /lib /lib32 /lib64

Where libraries are stored.<br>
Libraries are files that applications can use to perform various functions. They may be required by binaries in `/bin` and `/sbin`.

### /media /mnt

Where you would find your ather mounted drives.<br>
They can be usb stick, external drives etc. <br>
Nowadays the os mounts drives to `/media`<br>
When mounting things manualy use the `/mnt` directory and leave the os to `/media`

### /opt (optional)

Manually installed software resides here.<br>
You can also install software you created yourself.<br>

### /proc

Contains pseudo files that contain info about system processes and resources<br>
Every process will have a directory here which contains info on that process.<br> 
Every directory is a pid. 

### /root

Root users home directory. Does not contain regular home files and directories <br>
and does not reside in `/home` directory 

### /run 

It is a tempfs file system meaning it runs in memory. <br>
Everything in it is deleted when the os reboots or powersdown.<br>
Used for processes that start early in the boot procedure <br>
that the use to store runtime information that they use to function.

### /snap 

Where snap applications are stored and mainly used by ubuntu.<br>
Self-contained appplications. <br>

### /srv (service)

Service data is stored here. <br>
e.g is you run a server or ftp this is where you would store <br>
the files that would be accesed by an external user. <br>
For better security

### /sys (system)

A way to interact with the kernel. <br>
e.g Changing settings to a graphics card in a hybrid system <br>
It is similar to `/run` and is not phisically written to the <br>
disk, it is created everytime the system is booted up.

### /temp (Temporary)

Files are stored temporarily b applications that could be used <br>
during a session. e.g when edditing a document <br>

### /usr (user or UNIX system resource)

User application space where applications will be installed <br>
that are used by the user as opposed to the bin directory <br>
is used by system and admin. Any application stored here <br>
are non essential for basic system operation installed <br> applications. 

### /var (variable)

Contains directories that are expected to grow in size <br>


### /sbin (system binaries)

Binaries that the root(system Admin) would use. <br>
A standard user has no access to.
