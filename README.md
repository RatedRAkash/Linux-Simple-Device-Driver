## Linux-Simple-Device-Driver
It is a Simple Linux Device Driver Project. Whenever a User-Application (e.g. `cat` command or other User-Program) tries to communicate with `read` operation on a `device-driver`, a `system-call` happens and Kernel handles gets control over the CPU. Then the Kernel invokes the implementation of `read` operation code for the corresponding device-driver we have implemented.

### Build Project using Makefile
```
# to build project
make all

# to clean project
make clean
```

### Command
```
# insert Module(Device Driver) to Linux Kernel
sudo insmod ramos_ldd.ko

# remove Module(Device Driver) to Linux Kernel
sudo rmmod ramos_ldd.ko

# it shows all the Module(Device Driver) in Linux Kernel
sudo lsmod

# To see system log(kernel print messages)
sudo dmesg
sudo dmesg -c
tail /var/log/syslog

# To see “Module(Device Driver)” INFORMATION
modinfo ramos_ldd.ko
```