# Debian-10-Buster-Static-IP-assign

vim  /etc/network/interfaces

~~~
# Include files from /etc/network/interfaces.d:
source-directory /etc/network/interfaces.d

# Cloud images dynamically generate config fragments for newly
# attached interfaces. See /etc/udev/rules.d/75-cloud-ifupdown.rules
# and /etc/network/cloud-ifupdown-helper. Dynamically generated
# configuration fragments are stored in /run:

source-directory /run/network/interfaces.d
allow-hotplug ens3
iface ens3 inet static
address 192.168.1.10
netmask 255.255.255.0
gateway 118.67.1.1
dns-nameservers 8.8.8.8


allow-hotplug ens8
iface ens8 inet static
address 192.168.2.15
netmask 255.255.255.0
~~~
~~~
save and exit
the 
systemctl restart networking
~~~
