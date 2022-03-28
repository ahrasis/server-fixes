# server fixes

I will compile some of my server install / build fixes in here.

# proxmox install on debian mate / lxde

Just make sure you first remove default qemu that comes with debian mate / lxde before you start installing proxmox: "apt -f remove qemu-system-data". I may make a script but I don't think it is necessary for now.

# network interfaces sample

auto lo
iface lo inet loopback

auto eno4
iface eno4 inet static
        address 192.168.0.198
        netmask 255.255.255.0
        network 192.168.0.0
        broadcast 192.168.0.255
        gateway 192.168.0.1

iface eno4 inet6 static
	address 2001:f40:909:2482:862b:2bff:fe5f:dd02
	netmask 64
	gateway 2001:f40:909:2482:76da:88ff:fe7e:328d
