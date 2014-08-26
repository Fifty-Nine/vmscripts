== vmscripts ==
Some scripts I hacked together for managing my KVM virtual machines on 
OpenIndiana/illumos with ZFS. Assumes all your VMs are in zfs datasets
under /vmtank. The structure of a VM looks like this:

	- vmtank/$VM
		- config.sh - configuration variables. See vm-clone.
		- disk0 - a ZFS volume that's used as the first disk.
		- monitor - a unix-domain socket connected to the VM's monitor
		-	pid - a file containing the PID of a running VM

These scripts were thrown together over the course of a couple days and
make lots of assumptions about my setup, so use at your own risk!

